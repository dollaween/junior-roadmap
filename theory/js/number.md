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

Оператор **"Остаток от деления"** (`%`) — возвращает целый остаток от деления левого операнда на правый.

Дополнительные математические операции и константы содержатся в объекте `Math`.

К числовому типу данных также относятся `Infinity`, `-Infinity` и `NaN`.

---

Оператор **"Инкремент"** (`++`) — увеличивает на единицу операнд и возвращает значение.

Имеет две формы:
* Постфиксный инкремент — значение возвращается, а затем увеличивается на единицу.
* Префиксный инкремент — значение увеличивается на единицу, а затем возвращается.

Пример постфиксного инкремента
```js
let x = 10
let y = x++

// значение 
console.log(x)  // 11
console.log(y)  // 10
// так как значение сперва возвращается, то в `y` будет записано 10
// и только потом значение `x` увеличивается на единицу
```

Пример префиксного инкремента
```js
let x = 10
let y = ++x

console.log(x)  // 11
console.log(y)  // 11
// так как значение сперва увеличивается на единицу и только потом возвращается, то в `y` попадет число `11`
```

---

Оператор **"Декремент"** (`--`) — уменьшает на единицу операнд и возвращает значение.

По аналогии с инкрементом, имеет две формы:
* Постфиксный декремент — значение возвращается, а затем уменьшается на единицу.
* Префиксный декремент — значение уменьшается на единицу, а затем возвращается.

```js
// постфиксный
let a = 4
let b = a--
console.log(a) // 3
console.log(b) // 4

// префиксный
let x = 4
let y = --x
console.log(x) // 3
console.log(y) // 3
```

---

Для более лаконичных записей, существуют сокращенные записи оператора присваивания:

| Название | Сокращенный оператор | Полная запись |
| --- | --- | --- |
| Присваивание со сложением | `x += y` | `x = x + y` |
| Присваивание с вычитанием | `x -= y` | `x = x - y` |
| Присваивание с умножением | `x *= y` | `x = x * y` |
| Присваивание с делением | `x /= y` | `x = x / y` |
| Присваивание по модулю | `x %= y` | `x = x % y` |

Примеры:
```js
let x = 10
let y = 5

x += y  // x === 15
x -= y  // x === 5
x *= y  // x === 50
x /= y  // x === 2
x %= y  // x === 0
```

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

С остальными методами и свойствами числа можно ознакомиться на MDN:
[https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Number](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Number)


---

Источники:
* [Number](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Number)
* [Infinity](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Infinity)
* [NaN](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/NaN)
* [Арифметические операции](https://developer.mozilla.org/ru/docs/conflicting/Web/JavaScript/Reference/Operators#remainder)
* [Math](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Math)