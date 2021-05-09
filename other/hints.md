<div align="center">

# Подсказки

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


<div align="center">

### Пояснение

</div>

---

Ниже представлена краткая справка в очень сжатом виде. Рекомендуется держать перед глазами при решении задач.

`->` — означает что будет возвращено при вызове функции/метода, обращении к свойству.

---

<div align="center">

### Числа

</div>

---

Создание:
```js
const num = 10
```

Математические операторы:
```js
+, -, /, *, **, %, ++, --
```

Приведение к числу:
```js
Number(any)     -> number / NaN
parseInt(any)   -> number / NaN
parseFloat(any) -> number / NaN
number / 0      -> Infinity
-number / 0     -> -Infinity
NaN * number    -> NaN
```

---

<div align="center">

### Строки

</div>

---

Создание:
```js
const str = 'string'
const str = new String()
```

Строки неизменяемы!
```js
str.length          -> длина строки
str[0]              -> первый символ
str[str.length - 1] -> последний символ
```

Кавычки
```js
'I\'m programmer'    -> "I'm programmer"
`My name is ${name}` -> 'My name is John'
```

Преобразования
```js
parseInt(str)   -> number / NaN
parseFloat(str) -> number / NaN
Number(str)     -> number / NaN
any + string    -> string, например (5 + '10' -> '510')
```

Методы поиска
```js
charAt(index)   -> string
includes(str)   -> boolean
startsWith(str) -> boolean
endsWith(str)   -> boolean
```

Методы работы
```js
toLowerCase()           -> string
toUpperCase()           -> string
trim()                  -> string
replace(target, substr) -> string
substring(start, stop)  -> string
slice(start, stop)      -> string
split(str)              -> array
```

---

<div align="center">

### Массивы

</div>

---

Создание
```js
const arr = []
const arr = new Array()
const arr = Array.of(elem)
const arr = Array.from(arrayLike)
```

Методы изменения (изменяют текущий массив)
```js
* push(elem)           -> длина массива
* pop()                -> удаленный элемент
* unshift(elem)        -> длина массива
* shift()              -> удаленный элемент
* reverse()
* splice(start, count) -> удаленные элементы
```

Методы доступа
```js
indexOf(elem)          -> index
lastIndexOf(elem)      -> index
slice(start, end)      -> array
concat(arr)            -> array
join(separator)        -> string
toString()             -> string
```

Методы обхода
```js
forEach(fn)
map(fn)            -> array
every(fn)          -> boolean
some(fn)           -> boolean
filter(fn)         -> array
reduce(fn, params) -> value
```

Разное
```js
arr.length          -> длина массива
arr[0]              -> первый элемент
arr[arr.length - 1] -> последний элемент
```

Проверка
```js
Array.isArray(obj) -> boolean
```

---



