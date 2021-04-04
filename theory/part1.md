<div align="center">

# Часть 1

[Главная](https://github.com/dollaween/junior-roadmap/)
|
[Карта](/roadmap/README.md)
|
[Тесты](/tests/README.md)
|
[Задачи](/tasks/README.md)

</div>

---

* `console.log()` — выводит сообщение в консоль.

---

## Переменные
**Переменная** — именованная часть памяти, в которую могут помещаться разные значения переменной.

---

`let` — объявляет переменную с блочной областью видимости.

```js
// объявляем переменную
let number = 2

// значение переменной можно менять
number = 4
number = 6 + 3

// объявлять в одной области видимости несколько переменных с одинаковым именем нельзя
let variable = 1
let variable = 3  // SyntaxError: Identifier 'variable' has already been declared
```

---

`var` — объявляет переменную область видимости которой является вся функция.

```js
var password = '12345'
password = 'qwerty'
```

* [mdn](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/var)

---

`const` | [mdn](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/const) — объявляет константу. Значение константы менять нельзя.

```js
const planet = 'Earth'

// значение констант менять нельзя
planet = 'Mars' // TypeError: Assignment to constant variable.
```

---

Подробнее:
* [let](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/let)
* [var](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/var)
* [const](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/const)

---


## Числа





















