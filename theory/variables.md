<div align="center">

# Переменные

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

**Значение (value)** — это какой-то фрагмент информации.  
Значения делятся на два типа:
1. Фиксированные значения (литералы)
2. Изменяемые значения (переменные)

```js
10       // литерал числа
'Hello'  // литерал строки
true     // литерал логического типа

let num  // переменная
```

---

**Переменная (variable)** — именованная часть памяти, в которую могут помещаться разные значения переменной.

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

Оператор **"Присваивание"** (`=`) — присваивает левому операнду значение, основанное на значнии правого операнда.

```js
// присваивает переменной `login` значение `John`
const login = 'John'

// цепочка операторов присваивания задает нескольким переменным одно и то же значение
const x = y = 10
console.log(x)  // 10
console.log(y)  // 10
```

---

Источники:
* [let](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/let)
* [var](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/var)
* [const](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/const)
* [Операторы присваивания](https://developer.mozilla.org/ru/docs/conflicting/Web/JavaScript/Reference/Operators_8d54701de06af40a7c984517cbe87b3e)
