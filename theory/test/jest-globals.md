<div align="center">

# Jest — глобальные функции и объекты

[Главная](https://github.com/dollaween/junior-roadmap/)
|
[Карта](/roadmap/README.md)
|
[Теория](/theory/README.md)
|
[Тесты](/tests/README.md)
|
[Задачи](/tasks/README.md)

</div>

---

Нижеприведенные функции и объекты доступны в глобальной области видимости.

Функции, полезные для сброса глобальных состояний:
- [`afterAll(fn, timeout)`](https://jestjs.io/docs/api#afterallfn-timeout) — запускает функцию `fn` после всех тестов.
- [`afterEach(fn, timeout)`](https://jestjs.io/docs/api#aftereachfn-timeout) — запускает функцию `fn` после каждого тесте.
- [`beforeAll(fn, timeout)`](https://jestjs.io/docs/api#beforeallfn-timeout) — запускает функцию `fn` перед всеми тестами.
- [`beforeEach(fn, timeout)`](https://jestjs.io/docs/api#beforeeachfn-timeout) — запускает функцию `fn` перед каждым тестом.

Функции и объекты группировки нескольких тестов:
- [`describe(name, fn)`](https://jestjs.io/docs/api#describename-fn) — группирует в один блок несколько тестов.
- [`describe.each(table)(name, fn, timeout)`](https://jestjs.io/docs/api#describeeachtablename-fn-timeout) — запускает один и тот же тест, но с несколькими входными параметрами.
- [`describe.only(name, fn)`](https://jestjs.io/docs/api#describeeachtablename-fn-timeout) — запускает тесты только в текущем `describe`-блоке, все остальные будут пропущены.
- [`describe.only.each(table)(name, fn)`](https://jestjs.io/docs/api#describeonlyeachtablename-fn) — запускает тесты только в текущем `describe`-блоке с несколькими наоборами входных параметров.
- [`describe.skip(name, fn)`](https://jestjs.io/docs/api#describeskipname-fn) — пропускает текущий `describe`-блок.
- [`describe.skip.each(table)(name, fn)`](https://jestjs.io/docs/api#describeskipname-fn)


- `test(name, fn, timeout)`
- `test.concurrent(name, fn, timeout)`
- `test.concurrent.each(table)(name, fn, timeout)`
- `test.concurrent.only.each(table)(name, fn)`
- `test.concurrent.skip.each(table)(name, fn)`
- `test.each(table)(name, fn, timeout)`
- `test.only(name, fn, timeout)`
- `test.only.each(table)(name, fn)`
- `test.skip(name, fn)`
- `test.skip.each(table)(name, fn)`
- `test.todo(name)`

Подробнее про каждый из них можно прочесть в официальной документации: [Globals](https://jestjs.io/docs/api).

---

Источники:
- [Globals](https://jestjs.io/docs/api)
