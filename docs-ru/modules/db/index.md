Title: Базы данных

# Базы данных

Модуль базы данных `stappler_db`.

Система поддерживает доступ к СУБД [PostgreSQL](postgres.md) и [SQLite](sqlite.md).

Все системы работы с БД используют интерфейс пулов памяти.

## Интерфейс приложения

Для работы с БД необходимо определить интерфейс приложения. Для простых приложений можно использовать тип `db::SimpleServer` (`SPDbSimpleServer.h`). Для более сложных взаимодействий необходимо перегружать класс `db::ApplicationInterface` (`SPDbAdapter.h`) вручную или использовать встроенные в подсистему механизмы (ресурсный модуль `xenolith_resource_storage`, компоненты для веб-сервера).

## Схемы данных

Интерфейс БД основан на схемах данных. Пример определения схемы:

```cpp
#include "SPScheme.h"

using namespace stappler::db;

Scheme _objects;

_objects.define(Vector<Field>{
	Field::Text("text", MinLength(3), Flags::Indexed),
	Field::Extra("data", Vector<Field>{
		Field::Array("strings", Field::Text("")),
	}),
	Field::Set("subobjects", _subobjects),
	Field::File("file", MaxFileSize(1_MiB)),
	Field::Text("alias", Transform::Alias),
	Field::Integer("mtime", Flags::AutoMTime | Flags::Indexed),
	Field::Integer("index", Flags::Indexed),
	Field::View("refs", _refs, ViewFn([this] (const Scheme &objScheme, const Value &obj) -> bool {
		return true;
	}), FieldView::Delta),

	Field::Array("array", Field::Extra("", Vector<Field>{
		Field::Integer("one"),
		Field::Integer("two"),
	})),

	Field::Extra("textFile", Vector<Field>{
		Field::Text("type"),
		Field::Integer("mtime"),
		Field::Text("content"),
	}),
	Field::Extra("binaryFile", Vector<Field>{
		Field::Text("type"),
		Field::Integer("mtime"),
		Field::Bytes("content"),
	}),

	Field::Set("images", _images, Flags::Composed),
},
AccessRole::Admin(AccessRoleId::Authorized));
```

Тип `Field` предназначен для определения полей схемы. Доступные типы полей:

* `Data` - нетипизированные данные
* `Integer` - целое число
* `Float` - число с плавающей точкой
* `Boolean` - логический тип
* `Text` - текст
* `Bytes` - бинарные данные
* `Password` - специальный тип для хранения паролей
* `Extra` - нетипизированные данные, следующие определённой схеме
* `File` - внешний файл
* `Image` - внешнее изображение
* `Object` - связь с объектом другой схемы
* `Set` - связь с набором объектов другой схемы
* `Array` - массив из других полей
* `View` - отображение другой схемы с возможностью фильтрации
* `FullTextView` - полнотекстовое отображение, используется для полнотекстового поиска
* `Virtual` - виртуальное (вычислимое) поле. Вызывает определённые функции чтения и записи при доступе к полю
* `Custom` - поле с пользовательским определением (примеры в `SPDbFieldExtensions.h`)

Режим работы полей модифицируется флагами (`db::Flags`), трансформациями (`db::Transform`), фильтрующими функциями (`db::ReadFilterFn, db::WriteFilterFn, db::ReplaceFilterFn`), специализированными параметрами конфигурации (см. `SPDbField.h`). Все моификаторы передаются в произвольном порядке в конструктор поля.

Для запроса к данным необходимо получить доступ к транзакции БД. Способ получения зависит от реализации `ApplicationInterface`.

В схеме всегда определено поле `__oid` типа `Integer`, представляющее внутренний уникальный идентификатор. Как правило, оно уникально внутри системы в целом (за исключением схем с флагом `Scheme::Detached`).

После получения можно выполнять запросы к данным с помощью функций `Scheme`:

```cpp
class Scheme {
public:
	// описание основных прототипов, полный список вариантов в SPDbWorker.h в классе Worker.
	// В реальном коде функции ретранслируются в класс Worker, и проверка прототипа выполняется там

	auto get(const Transaction &&, int64_t, UpdateFlags) const -> Value;
	auto foreach(const Transaction &t, const Query &,
			const Callback<bool(Value &)> &) const -> bool;
	auto select(const Transaction &t, const Query &) const -> Value;
	auto create(const Transaction &t, const Value &, UpdateFlags) const -> Value;
	auto update(const Transaction &t, int64_t, const Value &, UpdateFlags) const  -> Value;
	auto remove(const Transaction &t, int64_t) const -> bool;
	auto count(const Transaction &t, const Query &) const -> size_t;
	auto touch(const Transaction &t, int64_t) const -> void;

	auto getProperty(const Transaction &t, int64_t, StringView field) const -> Value;
	auto setProperty(const Transaction &t, int64_t, StringView field, const Value &) const -> Value;
	auto appendProperty(const Transaction &t, int64_t, StringView field, const Value &) const -> Value;
	auto clearProperty(const Transaction &t, int64_t, StringView field) const -> bool;
	auto countProperty(const Transaction &t, int64_t, StringView field) const -> size_t;
};
```

Функции доступа к свойствам работают на конкретное поле объекта, это поле должно относиться к типам `File, Image, Object, Set, Array`.

## Тип запроса

Тип `db::Query` предназначен для выполнения запросов к БД.

```cpp
#include "SPDbQuery.h"

namespace stappler::db {

class Query : public AllocBase {
public:
	// Тип поля для включения или исключения
	struct Field : public AllocBase {
		String name;
		Vector<Field> fields;
	};

	// Тип для хранения ограничения запроса
	struct Select : public AllocBase {
		Comparation compare = Comparation::Equal;
		Value value1;
		Value value2;
		String field;
		FullTextQuery textQuery;
	};

	static Query all(); // запрос ко всем объектам схемы
	static Query field(int64_t id, const StringView &); // запрос к полю конкретного объекта
	static Query field(int64_t id, const StringView &, const Query &); // запрос к полю конкретного объекта

	Query & select(const StringView &alias); // запрос по псевдониму
	Query & select(int64_t id); // запрос по __oid
	Query & select(const Value &); // запрос по псевдониму, __oid или уже полученному объекту
	Query & select(Vector<int64_t> &&id); // запрос списка объектов по __oid

	// ограничение запроса
	Query & select(const StringView &f, Comparation c, const Value & v1, const Value &v2 = Value());
	Query & select(const StringView &f, const Value & v1); // специальный случай для точного соотвествия
	Query & select(const StringView &f, FullTextQuery && v);
	Query & select(Select &&q);

	// упорядочивание результата
	Query & order(const StringView &f, Ordering o = Ordering::Ascending, size_t limit = stappler::maxOf<size_t>(), size_t offset = 0);
	
	// запрос по мягкому лимиту (ContinueToken)
	Query & softLimit(const StringView &, Ordering, size_t limit, Value &&);
	Query & first(const StringView &f, size_t limit = 1, size_t offset = 0);
	Query & last(const StringView &f, size_t limit = 1, size_t offset = 0);

	// запрос по страничному лимиту
	Query & limit(size_t l, size_t off);
	Query & limit(size_t l);
	Query & offset(size_t l);

	// дельта-запрос
	Query & delta(uint64_t);
	Query & delta(const StringView &);

	// включить поля в запрос
	template <typename ... Args>
	Query & include(Field &&, Args && ...);

	Query & include(Field &&);
	
	// Исключить поле из запроса
	Query & exclude(Field &&);

	// Блокирует объект при получении до обновления
	Query & forUpdate();
};

}
```

## Путь прохождения запроса

* Создаётся объект `Worker` (`SPDbWorker.h`), соответствующий текущему запросу. Данный объект интерпретирует аргументы запроса и конвертирует их в удобное для системы внутреннее представление (например, запрос `get` конвертируется в `select`). Также, `Worker` создаёт или захватывает текущую активную транзакцию (`Transaction`: `SPDbTransaction.h`). 
* Созданный `Worker` передаётся назад в `Scheme`, вызывая соответствующую конкретную реализацию запроса (например, `updateWithWorker`, `SPDbScheme.cc:523`). Эта функция производит фильтрацию и адаптацию входящих данных, добавляет автоматические значения, значения по умолчанию. Эта функция может выйти с ошибкой если переданные данные не могут использоваться для запроса на основании описания полей (например, не определено требуемое поле). Также, проводится дополнительный анализ, например, выбор между стратегиями `patch` (разовый запрос на обновление в БД) и `update` (запрос, работающий по парадигме чтение-модификация-запись).
* Данные запроса и `Worker` передаются в `Transaction` с соответствующим запросом. Транзакция выполняет проверку уровня доступа для запроса и может завершить запрос, если проверка не проходит. Проверка уровня доступа также может модифицировать запрос, добавляя параметры. В ходе проверки уровня доступа могут выполняться дополнительные запросы к БД, такие запросы активно кешируются в транзакции.
* Транзакция передаёт запрос и `Worker` в `Adapter` (`SPDbAdapter.h`). Адаптер реализует функции виртуальных полей, контролирует другие вычислимые поля, такие, как `View`. На момент получения адаптером запроса можно быть уверенным, что запрос корректен с позиции схемы данных и контроля доступа, а значит, его выполнение ограничено лишь технической реализацией доступа к БД.
* Адаптер передаёт запрос непосредственно в интерфейс к БД, связанный с транзакцией, на исполнение. Этот интерфейс реализует непосредственно преобразование логического представления запроса в соответствующий текст SQL либо функции БД.
* Успешно полученный результат проходит через `Adapter`. Выполняются функции, контролирующие работу автоматических полей, если необходима модификация объектов других схем данных.
* Результат из адаптера возвращается в транзакцию. Выполняется фильтрация результата на основании контроля доступа.
* Результат возвращается в схему данных. На этом этапе выполняются функции преобразования выходных данных в их конечное представление.
* Результат возвращается пользователю.
В некоторых случаях удобно создать объект `Worker` вручную. Например, для определения текущего запроса как системного на уровне контроля доступа либо при наличии нескольких активных транзакций.

## Автоматизация полей

См. [автоматизация полей](auto.md)

## Связи между полями

См. [связи между полями](linkage.md)

## Мягкий лимит и ContinueToken

См. [связи между полями](pagination.md)

## Прочие функции

Сжатие на ходу работает для полей типа `Data` и `Extra` с заданным флагом `Flags::Compressed`.

Для поддержки дельта-запросов на уровне схемы необходимо явно указывать флаг `Scheme::WithDelta`. На уровне отображения `FieldView::Delta`. После этого дельта-запросы будут доступны через тип `Query`.

`Adapter` реализует функции хранилища ключ-значение:
* `get` - получает значение по ключу
* `set` - устанавливает значение для ключа
* `clear` - удаляет значение для ключа
Ключом могут выступать любые бинарные данные (что удобно при использовании хешей), и по умолчанию ни одно значение не хранится вечно.
