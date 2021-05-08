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

### Массивы

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
* push(elem)           -> array length
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
