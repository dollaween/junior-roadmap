<div align="center">

# Числа

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

Дополнительные математические операции и константы содержатся в объекте `Math`.

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

`Math` — встроенный объект, хранящий в своих свойствах и методах различные математические константы и функции.

```js
// возвращает абсолютное значение числа
Math.abs(-10)  // 10

// возвращает значение числа, округленное к меньшему целому
Math.floor(2.7)  // 2

// возвращает значение числа, округленное к большему целому
Math.ceil(2.1)  // 3

// возвращает значение числа, округленное к ближайшему целому
Math.round(2.1)  // 2
Math.round(2.7)  // 3
Math.round(2.5)  // 3

// возвращает наибольшее число из своих аргументов
Math.max(4, 1, 5, 2)  // 5

// возвращает наименьшее число из своих аргументов
Math.min(4, 1, 5, 2)  // 1

// возвращает псевдослучайное число в диапазоне от 0 до 1 (не включительно)
Math.random()  // 0.759685260672438
```

---

Источники:
* [Number](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Number)
* [Infinity](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Infinity)
* [NaN](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/NaN)
* [Арифметические операции](https://developer.mozilla.org/ru/docs/conflicting/Web/JavaScript/Reference/Operators#remainder)
* [Math](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Math)