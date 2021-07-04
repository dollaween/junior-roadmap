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

Нижеприведенные методы доступны в глобальной области видимости.

---

<div align="center">

### `test` (`it`)

</div>

---

> `it` является алиасом для `test`.

`test` — это методы, которые запускают тесты.

- [`test(name, fn, timeout)`](https://jestjs.io/docs/api#describeskipname-fn) — запускает функцию `fn`.
- [`test.each(table)(name, fn, timeout)`](https://jestjs.io/docs/api#testeachtablename-fn-timeout) — запускает функцию `fn` с несколькими наборами входных параметров.
- [`test.only(name, fn, timeout)`](https://jestjs.io/docs/api#testeachtablename-fn-timeout) — запускает только указанный тест, игнорируя все остальные.
- [`test.only.each(table)(name, fn)`](https://jestjs.io/docs/api#testonlyeachtablename-fn-1) — запускает только уазанный тест с несколькими наборами параметров.
- [`test.skip(name, fn)`](https://jestjs.io/docs/api#testskipname-fn) — пропускает текущий тест.
- [`test.skip.each(table)(name, fn)`](https://jestjs.io/docs/api#testtodoname)
- [`test.todo(name)`](https://jestjs.io/docs/api#testtodoname) — отмечает, какой тест необходимо написать.

```js
test('did not rain', () => {
  expect(inchesOfRain()).toBe(0)
})
```

Пример с промисом
```js
test('has lemon in it', () => {
  return fetchBeverageList().then(list => {
    expect(list).toContain('lemon')
  })
})
```

Пример с `each`
```js
test.each([
  [1, 1, 2],
  [1, 2, 3],
  [2, 1, 3],
])('.add(%i, %i)', (a, b, expected) => {
  expect(a + b).toBe(expected)
})

test.each([
  { a: 1, b: 1, expected: 2 },
  { a: 1, b: 2, expected: 3 },
  { a: 2, b: 1, expected: 3 },
])('.add($a, $b)', ({ a, b, expected }) => {
  expect(a + b).toBe(expected)
})
```

---

<div align="center">

### `describe`

</div>

---

`describe` — это методы для группировки нескольких тестов.

- [`describe(name, fn)`](https://jestjs.io/docs/api#describename-fn) — группирует в один блок несколько тестов.
- [`describe.each(table)(name, fn, timeout)`](https://jestjs.io/docs/api#describeeachtablename-fn-timeout) — запускает один и тот же тест, но с несколькими входными параметрами.
- [`describe.only(name, fn)`](https://jestjs.io/docs/api#describeeachtablename-fn-timeout) — запускает тесты только в текущем `describe`-блоке, все остальные будут пропущены.
- [`describe.only.each(table)(name, fn)`](https://jestjs.io/docs/api#describeonlyeachtablename-fn) — запускает тесты только в текущем `describe`-блоке с несколькими наборами входных параметров.
- [`describe.skip(name, fn)`](https://jestjs.io/docs/api#describeskipname-fn) — пропускает текущий `describe`-блок.
- [`describe.skip.each(table)(name, fn)`](https://jestjs.io/docs/api#describeskipname-fn)

```js
describe('my beverage', () => {
  test('is delicious', () => {
    expect(myBeverage.delicious).toBeTruthy()
  })

  test('is not sour', () => {
    expect(myBeverage.sour).toBeFalsy()
  })
})
```

---

<div align="center">

### Другие глобальные методы

</div>

---

Методы, полезные для сброса глобальных состояний:
- [`afterAll(fn, timeout)`](https://jestjs.io/docs/api#afterallfn-timeout) — запускает функцию `fn` после всех тестов.
- [`afterEach(fn, timeout)`](https://jestjs.io/docs/api#aftereachfn-timeout) — запускает функцию `fn` после каждого тесте.
- [`beforeAll(fn, timeout)`](https://jestjs.io/docs/api#beforeallfn-timeout) — запускает функцию `fn` перед всеми тестами.
- [`beforeEach(fn, timeout)`](https://jestjs.io/docs/api#beforeeachfn-timeout) — запускает функцию `fn` перед каждым тестом.


```js
afterEach(() => {
  cleanUpDatabase(globalDatabase);
})
```


---

Источники:
- [Globals](https://jestjs.io/docs/api)
