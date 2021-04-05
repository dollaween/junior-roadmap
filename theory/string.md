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

Метод `charAt()` — возвращает указанный символ из строки находящийся на заданном индексе.

Если символ не найден будет возвращена пустая строка.

```js
const str = 'What do you think?'

str.charAt(0)   // 'W'
str.charAt(5)   // 'd'
str.charAt(99)  // ''
```

---

Метод `includes()` — возвращает `true`, если строка содержит заданную подстроку.

```js
const str = 'Flawless victory'

str.includes('Flawless')   // true
str.includes('vic')        // true
str.includes('Confident')  // false
```

---

Метод `startsWith()` — возвращает `true`, если строка начинается с заданной подстроки.

```js
const domain = 'http://github.com'

domain.startsWith('http:')   // true
domain.startsWith('https:')  // false
```

---

Метод `endsWith()` — возвращает `true`, если строка заканчивается заданной подстрокой.

```js
const email = 'example@mail.com'

email.endsWith('mail.com')   // true
email.endsWith('yandex.ru')  // false
```

---

<div align="center">

### Методы работы со строкой

</div>

---

Метод `toLowerCase()` — возвращает значение строки преобразованной в нижний регистр.

Метод `toUpperCase()` — возвращает значение строки преобразованной в верхний регистр.

```js
const nickname = 'AwEsOmE NiCkNaMe'

nickname.toLowerCase()  // awesome nickname
nickname.toUpperCase()  // AWESOME NICKNAME
```

---

Метод `trim()` — вырезает пробельные символы с начала и конца строки.

```js
const stringWithSpace = '    Spaceman  '

stringWithSpace.trim()  // 'Spaceman'
```

---

Метод `replace()` — заменяет заданную подстроку другой строкой и возвращает получившийся результат.

```js
const age = 'My age is 20'

age.replace('20', '21')                       // 'My age is 21'
age.replace('My age is 20', 'I\'m, too old')  // "I'm too old"
```

---

Метод `substring(start, stop)` — возвращает подстроку от индекса `start` до индекса `stop` (не включительно).

```js
const greet = 'Have a nice day'

greet.substring(0, 4)   // 'Have'
greet.substring(7, 11)  // 'nice'

// если не указать индекс 'stop', то вернется строка от индекса 'start' и до конца
greet.substring(12)  // 'day'

// если ничего не найдено, то вернется пустая строка
greet.substring(90)  // ''

// при передаче отрицательного аргумента или NaN — он будет изменен на 0
greet.substring(-10)  // 'Have a nice day'

// если индекс 'start' больше индекса 'stop', то они будут изменены местами
greet.substring(11, 7)  // 'nice'
```

---

Метод `slice(start, stop)` — возвращает подстроку от индекса `start` до индекса `stop` (не включительно).

Метод ведет себя так же, как `substring()`, но с небольшими отличиями.

```js
const greet = 'Have a nice day'

greet.slice(0, 4)   // 'Have'
greet.slice(7, 11)  // 'nice'

// если не указать индекс 'stop', то вернется строка от индекса 'start' и до конца
greet.slice(12)  // 'day'

// если ничего не найдено, то вернется пустая строка
greet.substring(90)  // ''

// если индекс 'start' больше индекса 'stop', то будет возвращена пустая строка
greet.slice(11, 7)  // ''

// если индекс `start` отрицательный, то отсчет идет с конца строки
greet.slice(-3)  // 'day'

// если индекс 'stop' отрицательный, то будет обрезано указанное количество символов с конца строки
greet.slice(7, -4)  // 'nice'
```

---

С остальными методами строки можно ознакомиться на MDN:
[https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String)

---

Источники:
* [parseInt()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/parseInt)
* [parseFloat()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/parseFloat)
* [charAt()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/charAt)
* [includes()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/includes)
* [startsWith()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/startsWith)
* [endsWith()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/endsWith)
* [toLowerCase()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase)
* [toUpperCase()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase)
* [trim()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/Trim)
* [replace()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/replace)
* [substring()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/substring)
* [slice()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/String/slice)


















