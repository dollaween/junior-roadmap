<div align="center">

# Строки

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

Строки имеют три вида записи.

Для превращения строки в число используются функции `parseInt()`, `parseFloat()` и оператор "Унарный плюс" (`+`).

Для поиска подстроки нам предоставлены методы `charAt()`, `includes()`, `startsWith()`, `endsWith()`.

Строки неизменяемы. Это значит, что любая функция и метод не изменяют оригинальную строку, а возвращают новую. Методы для работы со строками: `toLowerCase()`, `toUpperCase()`, `trim()`, `replace()`, `slice()`, `substring()`, `split()`.

---

Есть три вида записи строк:
* Одинарные кавычки `''`
* Двойные кавычки `""`
* Апострофы ``

```js
// одинарные кавычки ничем не отличаются от двойных
const hello = 'Hello'
const hi = "Hi"

// если в строке с одинарными кавычками вам нужно вставить символ одинарной кавычки, то есть два пути
// 1. Изменить внешние кавычки на двойные
"I'm programmer"
// 2. Перед символом одинарной кавычки поставить специальный символ `\`
'I\'m programmer'

// то же самое работает и с двойными кавычками
'We have "something" in storage'
"We have \"something\" in storage"

// все что внутри кавычек — это обычный текст, поэтому переменные в таких строках вызваны не будут
const name = 'John'
console.log('My name is ${name}')  // 'My name is ${name}'
```

В кавычках через апостроф можно вызывать переменные:
```js
const name = 'John'
console.log(`My name is ${name}`)  // 'My name is John'
```

---

**Конкатенация строк** — объединение нескольких строк в одну.

```js
const greet = 'Hello'
const target = 'world'

console.log(greet + target) // 'Helloworld'

// для объединения строк с пробелом, его можно вставить
console.log(greet + ' ' + target)
// либо использовать переменные в кавычках-апострофах
console.log(`${greet} ${target}`)

// либо в самой переменной добавить нужный пробел
const name = ' John'
console.log(greet + target)  // 'Hello John'
```

При конкатенации строк и чисел, число будет восприниматься как строка:
```js
5 + 'Hello'  // '5Hello'
'10' + 10    // '1010'
```

---

Свойство `length` — возвращает длину строки.

```js
console.log('This is string'.length)  // 14
```

---

<div align="center">

### Преобразование строки в число

</div>

---

Функция `parseInt()` — принимает строку и возвращает целое число.

Если преобразовать строку в число невозможнно, будет возвращено значение `NaN`.

```js
parseInt('10')            // 10
parseInt('2.5')           // 2
parseInt('2D game')       // 2
parseInt('My age is 20')  // NaN
parseInt('-3')            // -3
parseInt(true)            // NaN
```

---

Функция `parseFloat()` — принимает строку и возвращает число с плавающей точкой.

Если преобразовать строку в число невозможнно, будет возвращено значение `NaN`.

```js

parseFloat('10')            // 10
parseFloat('2.5')           // 2.5
parseFloat('2D game')       // 2
parseFloat('My age is 20')  // NaN
parseFloat('-3')            // -3
parseFloat(true)            // NaN
```

---

<div align="center">

### Методы поиска

</div>

---

Метод `charAt()` — возвращает указанный символ из строки.

Если символ не найден будет возвращена пустая строка.

```js
const str = 'What do you think?'

str.charAt(0)   // 'W'
str.charAt(5)   // 'd'
str.charAt(99)  // ''
```

---

Источники:
* [parseInt()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/parseInt)
* [parseFloat()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/parseFloat)


















