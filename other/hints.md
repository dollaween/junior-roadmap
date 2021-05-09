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

### Числа

</div>

---

Операторы:
```js
+, -, /, *, **, %, ++, --
```

Создание:
```js
const num = 10
```

Приведение к числу:
```js
Number(value)     -> number / NaN
parseInt(value)   -> number / NaN
parseFloat(value) -> number / NaN
number / 0        -> Infinity
-number / 0       -> -Infinity
NaN * number      -> NaN
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
`My name is ${var}` -> 'My name is John'
'I\'m programmer' -> "I'm programmer"
```

Преобразования
```js
parseInt(str)   -> number / NaN
parseFloat(str) -> number / NaN
Number(str)     -> number / NaN
value + string  -> string (5 + '10' -> '510')
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

| Метод | Возвращаемый результат | Описание |
| --- | --- | --- |
| `push(elem)` | длина массива | добавляет элемент в конец |
| `pop()` | удаленный элемент | удаляет последний элемент |
| `unshift(elem)` | длина массива | добавляет элемент в начало |
| `shift()` | удаленный элемент | удаляет первый элемент |
| `reverse()` | | переворачивает массив |
| `splice(start, count)` | удаленные элементы | удаляет элементы и вставляет новые |

Методы изменения (изменяют текущий массив)
```js
* push(elem)           -> длина массива
* pop()                -> deleted elem
* unshift(elem)        -> array length
* shift()              -> deleted elem
* reverse()
* splice(start, count) -> deleted elems
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



