Title: Полнотекстовый поиск

# Полнотекстовый поиск

Полнотекстовый поиск определяется, как поле `Field::FullTextView`.

Пример определения:

```cpp
// Конфигурация хранится независимо от схемы данных.
// Время жизни объекта конфигурации должно соответствовать времени жизни схемы данных 
search::Configuration _search;

Field::FullTextView("tsv", db::FullTextViewFn([this] (const db::Scheme &scheme, const db::Value &obj) -> db::FullTextVector {
	size_t count = 0;
	db::FullTextVector vec;

	count = _search.makeSearchVector(vec, obj.getString("key"), db::FullTextRank::A, count);
	for (auto &it : obj.getArray("text")) {
		count = _search.makeSearchVector(vec, it.getString(), db::FullTextRank::B, count);
	}

	return vec;
}),  db::FullTextQueryFn([this] (const db::Value &data) -> db::FullTextQuery {
	return _search.parseQuery(data.getString());
}), _search, Vector<String>({"key", "text"})),
```

Для работы полнотекстового поиска необходима функция `FullTextViewFn`. Она возвращает заполненный вектор поиска на основе исходного объекта, в котором будут включены определённые поля из списка.

Опциональная функция `FullTextQueryFn` определяет способ конвертации запроса к полю в полнотекстовый запрос.

Для запроса используется `Query`.

```cpp
_scheme.select(_transaction, Query().select(tsv, "test fulltext \"query\""));
```

Стандартный способ разбора запроса соотвествует [websearch_to_tsquery](https://www.postgresql.org/docs/current/textsearch-controls.html)

## Поисковая конфигурация

Тип `search::Configuration` предназначен для тонкой настройки полнотекствовго поиска, генерации поисковых сниппетов и выполнения запрсов без обращения к БД.

```cpp
#include "SPSearchConfiguration.h"

search::Configuration _search = search::Configuration(search::Language::Russian);
```

### Настройка поискового движка

Поисковой движок работает по алгоритму:

1. Парсер разбирает переданный текст на токены (см. `SPSearchParser.h`). Эта стадия не кастомизируется.
2. Опционально, проводится обработка после парсинга, токены разбиваются на подслова
2. Стеммер языка конвертирует токены в стемы (устойчивые к изменениям формы слов). Движок использует стеммеры из проекта Snowball. Для отдельных токенов можно определить свой стеммер.
3. Стемы, характеризуемые их позицией в исходном тексте, добавляются в поисковой индекс

```cpp
	// Устанавливает базовый язык поиска для стеммера из предустановленных.
	void Configuration::setLanguage(Language);
	
	// Устаналвивает функцию стемминга для токена определённого типа
	// Функция принимает на вход токен и должна вызвать предоставленный Callback с итоговыми стемами
	// Стемов должно быть один или больше
	// Функция должна вернуть false в случае отказа от работы и true при успешном стемминге
	using StemmerCallback = Function<bool(StringView, const Callback<void(StringView)> &)>;
	void Configuration::setStemmer(ParserToken, StemmerCallback &&);
	
	// Устанавливает дополнительный список стем, исключаемых из индекса
	// Список должен быть массивом StringView, который заканчивается пустым StringView ( StringView() )
	void Configuration::setCustomStopwords(const StringView *);
	
	// Устанавливает функцию предобработки, вызываемую после парсера, но перед стеммером
	// Для токена функция должна вернуть вектор из его сегментов, которые направляются на вход стеммеру
	using PreStemCallback = Function<Vector<StringView>(StringView, ParserToken)>;
	void Configuration::setPreStem(PreStemCallback &&);
```


### Выполнение запросов

С помощью конфигурации можно выполнять отдельные стадии полнотекстового поиска независимо, разбирать и выполнять поисковые запросы.

```cpp
	// Функция получает на вход стем, исходный токен и тип токена
	using StemWordCallback = Callback<void(StringView, StringView, ParserToken)>;

	// Разбирает отдельный токен определённой формы, false если не нашлось подходящео стеммера
	bool Configuration::stemWord(const StringView &, ParserToken, const StemWordCallback &) const;

	// Разбирает на стемы отдельный текстовый сегмент
	void Configuration::stemPhrase(const StringView &, const StemWordCallback &) const;
	
	// Разбирает на стемы отдельный текстовый сегмент в виде HTML
	void Configuration::stemHtml(const StringView &, const StemWordCallback &) const;

	// Разбирает на составляющие стемы поисковой запрос
	Vector<String> Configuration::stemQuery(const SearchQuery &query) const;

	// Записывает в поисковой вектор текстовый сегмент, возвращает число записанных слов
	// rank - поисковой ранг этого текста
	// counter - число ранее записанных слов (возврат из makeSearchVector для того же SearchVector)
	// stemCallback - опционально получает итоговые стемы
	// Для записи нескольких текстов в индекс результат makeSearchVector одного должен быть передан
	// в counter следующего
	size_t Configuration::makeSearchVector(SearchVector &, StringView phrase,
		SearchData::Rank rank = SearchData::Rank::Unknown, size_t counter = 0,
		const StemWordCallback &stemCallback = nullptr) const;

	// Кодирует поисковой вектор в его представление в PostgreSQL
	// Опционально можно переопределить ранг для записей, где он не был задан
	String Configuration::encodeSearchVectorPostgres(const SearchVector &, SearchData::Rank rank = SearchData::Rank::Unknown) const;

	// Кодирует поисковой вектор во внутренний сжатый формат для хранения вне БД
	Bytes Configuration::encodeSearchVectorData(const SearchVector &, SearchData::Rank rank = SearchData::Rank::Unknown) const;

	// Разбирает поисковой запрос по правилам websearch_to_tsquery (PostgreSQL)
	// если strict = true, останавливает разбор при ошибке, записывает ошибку в err
	SearchQuery Configuration::parseQuery(StringView, bool strict = false, StringView *err = nullptr) const;

	// Разбирает поисковой запрос из строки и проверяет, соотвествует ли ему поисковой вектор
	bool Configuration::isMatch(const SearchVector &, StringView) const;

	// Для запроса, проверяет, удовлетворяет ли поисковой вектор запросу
	bool SearchQuery::isMatch(const SearchVector &) const;

	// Для запроса, проверяет, удовлетворяет ли поисковой вектор (кодированный с помощью 
	// Configuration::encodeSearchVectorData) запросу
	bool SearchQuery::isMatch(const BytesView &) const;
```

### Генерация сниппетов

После получения результата полнотекстового поиска из БД, необходимо показать пользователю, на каких основаниях полнотекстовый движок показывает результат. Для этого предназначены функции создания сниппетов/хедлайнов.

Для разметки функции получают список стем для подсветки, их можно получить функциями стемминга в `Configuration` из запроса или другого текста

```cpp
	struct Configuration::HeadlineConfig {
		StringView startToken = StringView("<b>"); // способ отметить начало совпадающео токена
		StringView stopToken = StringView("</b>"); // способ отметить конец совпадающео токена

		StringView startFragment = StringView("<div>"); // Способ отметить начало фрагмента с совпадающим токеном
		StringView stopFragment = StringView("</div>"); // Способ отметить конец фрагмента с совпадающим токеном
		StringView separator = StringView("…"); // Разделитель между фрагментами

		size_t maxWords = DefaultMaxWords; // максимальное число слов (токенов) в фрагменте для подсветки
		size_t minWords = DefaultMinWords; // базовое число слов кроме найденного для подсветки во фрагменте
		size_t shortWord = DefaultShortWord; // длина, меньше которой токены не считаются словом

		Function<void(StringView, StringView)> fragmentCallback; // Функция возврата готовых фрагментов
	};

	// Создаёт сниппеты для голого текста
	String Configuration::makeHeadline(const HeadlineConfig &, const StringView &origin, const Vector<String> &stemList) const;

	// Создаёт сниппеты для текста в HTML
	// count - максимальное число фрагментов для поиска
	String Configuration::makeHtmlHeadlines(const HeadlineConfig &, const StringView &origin, const Vector<String> &stemList, size_t count = 1) const;

	// Универсальная функция создания сниппетов
	// использует функцию producer, которая, при вызове, поставляет в передаваемыую функцию фрагменты голого текста
	// аргумент tag передаётся в функцию fragmentCallback для идентификации фрагмента, где было найдено соотвествие
	String Configuration::makeHeadlines(const HeadlineConfig &,
		const Callback<void(const Function<bool(const StringView &frag, const StringView &tag)>)> &producer,
		const Vector<String> &stemList, size_t count = 1) const;
```

