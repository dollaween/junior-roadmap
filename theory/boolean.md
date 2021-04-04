<div align="center">

# Boolean

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

`Boolean` — логический тип данных, который может быть только двух значений: `true` (правда, истина), либо `false` (ложь).

В основном, используется в логических конструкциях `if ... else` или при работе с операторами `&&`, `||`, `!`, `>`, `<`, `>=`, `<=`, `==`, `===`.

Значения `0`, `null`, `false`, `NaN`, `undefined` преобразовываются в `false`. Все остальные значения преобразовываются в `true`.

---

Оператор "Логическое И" (`&&`) возвращает `true`, если оба его операнда истинны.

```js
* `console.log(true && true)` -> `true`
* `console.log(true && false)` -> `false`
* `console.log(false && true)` -> `false`
* `console.log(false && false)` -> `false`
```

---

Оператор "Логическое ИЛИ" (`||`) возвращает `true`, если один из его операндов истинен.

```js

* `console.log(true && true)` -> `true`
* `console.log(true && false)` -> `true`
* `console.log(false && true)` -> `true`
* `console.log(false && false)` -> `false`
```
---

Оператор "Логическое НЕ" (`!`) переводит `true` в `false`, и наоборот.

```js
console.log(!true)    // false
console.log(!false)   // true
console.log(!!true)   // true
console.log(!!false)  // false
```

---

Источники:
* [Логическое И](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND)


