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

<div align="center">

## Переменные

</div>

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

---

`const` — объявляет константу. Значение константы менять нельзя.

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

<div align="center">

## Числа

</div>

Числа можно складывать `+`, вычитать `-`, умножать `*`, делить `/`, возводить в степень `**` и брать остаток от деления `%`.

```js
// пример целого числа
let integer = 10

// пример числа с плавающей точкой
let float = 10.36

10 + 3 === 13
10 - 3 === 7
10 * 3 === 30
10 / 2 === 5
10 ** 2 === 100
10 % 3 === 1
```

Оператор **остаток от деления** (`%`) — возвращает целый остаток от деления левого операнда на правый.

К числовому типу данных также относятся `Infinity`, `-Infinity` и `NaN`.

---

`Infinity` — положительная бесконечность.

```js
// значение Inifnity больше любого другого числа
Infinity > 99999999   // true
Infinity > -Infinity  // true

// получить положительную бесконечность можно умножив любое число на Infinity
Infinity * 10  // Infinity
// либо разделив положительное число на ноль
10 / 0  // Infinity
```

---

`-Infinity` — отрицательная бесконечность.

```js
// значение -Infinity меньше любого другого числа
-Infinity < -1111111  // true

// получить отрицательную бесконечность можно умножив любое число на -Infinity
-Infinity * 10  // -Infinity
// либо разделив отрицательное число на ноль
-20 / 0  // -Infinity
```

---

`NaN` — не число (Not a Number), это возвращаемое значение в ситуациях, когда математические функции не срабатывают должным образом.

```js
10 * 'Hello'       // NaN
parseInt('World')  // NaN
Math.sqrt(-1)      // NaN
```

`NaN` всегда не равен любому другому значению.

```js
NaN === 15   // false
NaN === NaN  // false
NaN == NaN   // false
```

Чтобы определить, является ли значение `NaN`, используйте функцию `isNaN()`.

```js
isNaN('Hi' / 4) // true
```

---














