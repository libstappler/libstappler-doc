Title: Пагинация и ContinueToken

# Пагинация и ContinueToken

Система `ContinueToken` (`SPDbContinueToken.h`) обеспечивает такую итерацию.

Базовая идея построена на использовании опорного значения по определённому полю, чтобы от него отсчитывать текущую страницу. Для неуникальных полей такая страница может иметь больше элемментов, чем необходимо, что и делает такой лимит мягким. Такая система всегда имеет линейную производительность.

Пример перебора значений с использованием `ContinueToken`:

```cpp
StringView c;
auto orig = mem::pool::acquire();
auto p = mem::pool::create(orig);
bool ended = false;
size_t batch = 20000; // размер пакета для обработки

while (!ended) {
    if (auto t = db::Transaction::acquire()) {
   	 mem::perform([&] { // экономим память через операционный пул
   		 // здесь id - вторичный уникальный индекс
   		 auto token = c.empty() ? ContinueToken("id", batch, false) : ContinueToken(c);

   		 db::Query q;
   		 auto data = token.perform(_trades, t, q);

   		 ...

   		 if (token.getNumResults() < token.getCount()) {
   			 ended = true;
   		 } else {
   			 c = StringView(token.encodeNext()).pdup(orig);
   		 }
   	 }, p);
    }
    mem::pool::clear(p);
}
```

Под капотом используются функции `Query::softLimit`.
