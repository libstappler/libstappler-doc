Title: Автоматизация полей

# Автоматизация полей

## Значения по умолчанию

Значение по умолчанию можно задать двумя способами:
* Статически, передав `Value` в определение поля
* Динамически, передав `db::DefaultFn`. В функцию будут передаваться данные, с которыми создаётся объект.
* Неявно, с помощью флагов `Flags::AutoCTime, Flags::AutoMTime`

## Фильтрация

Фильтры позводяют изменить значение, которое будет сохранено в БД или выведено пользователю. Фильтры работают снаружи от контроля доступа.

* `ReadFilterFn = Function<bool(const Scheme &, const Value &obj, Value &value)>` - изменяет значение, которое будет возвращено пользователю на основании полученного из БД. При необходимости изме6нить значение, изменяется value. Чтобы скрыть значение, необходимо вернуть false.
* `WriteFilterFn = Function<bool(const Scheme &, const Value &patch, Value &value, bool isCreate)>` - изменяет значение для записи в БД на основании переданного пользователем. Для запрета записи нужно вернуть false.
* `ReplaceFilterFn = Function<bool(const Scheme &, const Value &obj, const Value &oldValue, Value &newValue)>` - вариант `WriteFilterFn`с доступом предыдущему значению поля. Работает медленнее.

## Вычислимые и виртуальные поля

Для вычислимых и виртуальных полей используется тип `Virtual`. Пример реализации:

```cpp

_virtualTest.define({
	Field::Text("name", MinLength(3)),
	Field::Virtual("computed", VirtualReadFn([] (const Scheme &, const Value &value) {
		Value tmp(value);
		tmp.erase("__oid");
		tmp.setInteger(Time::now().toMicros(), "time");
		return tmp;
	}), Vector<String>({"name"})),

	Field::Virtual("virtual", VirtualReadFn([] (const Scheme &, const Value &value) {
		auto path = filesystem::writablePath<Interface>(toString(value.getString("name"), ".cbor"));
		if (filesystem::exists(path)) {
			return data::readFile<Interface>(path);
		}
		return Value();
	}), VirtualWriteFn([] (const Scheme &objScheme, const Value &obj, Value &data) {
		auto path = filesystem::writablePath<Interface>(toString(obj.getString("name"), ".cbor"));
		data::save<Interface>(data, path);
		return true;
	}), Vector<String>({"name"}))
});
```

Виртуальные поля определяют, какие реальные поля необходимы для их работы в виде массивов имён. Гарантируется, что значение этих полей будет доступно в функциях `VirtualReadFn` и `VirtualWriteFn`.
