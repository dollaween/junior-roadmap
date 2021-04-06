<div align="center">

# Массивы

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

### Методы изменения массива

</div>

---

Нижеприведенные методы изменяют массив, на котором вызываются.

---

Метод `push()` — добавляет один или несколько элементов в конец массива и возвращает новую длину массива.

```js
const numbers = [1, 2, 3]

const length = numbers.push(4)

console.log(length)   // 4
console.log(numbers)  // [1, 2, 3, 4]
```

---

Метод `pop()` — удаляет последний элемент массива и возвращает его значение.

```js
const roles = ['admin', 'moderator', 'reviewer']

const deleted = roles.pop()

console.log(deleted)   // 'reviewer'
console.log(roles)  // ['admin', 'moderator']
```

---

Метод `unshift()` — добавляет один или несколько элементов в начало массива и возвращает новую длину массива.

```js
const furniture = ['table', 'chair', 'carpet']

const length = furniture.unshift('lamp', 'bed')

console.log(length)     // 5
console.log(furniture)  // ['lamp', 'bed', 'table', 'chair', 'carpet']
```

---

Метод `shift()` — удаляет первый элемент массива и возвращает его значение.

```js
const ids = [4, 8, 15, 16, 23, 42]

const deleted = ids.shift()

console.log(deleted)  // 4
console.log(ids)      // [8, 15, 16, 23, 42]
```

---

Метод `reverse()` — переворачивает массив — первый элемент становится последним и наоборот.

```js
const chars = ['A', 'B', 'C', 'D', 'E', 'F']

chars.reverse()

console.log(chars)  // ['F', 'E', 'D', 'C', 'B', 'A']
```

---

Метод `splice(start, deleteCount)` — удаляет существующие элементы и/или добавляет новые.

`start` — индекс, с которого начать удаление.

`deleteCount` — количество элементов, которые будут удалены.

```js
const colors = ['blue', 'red', 'yellow', 'green']

const deletedColors = colors.splice(0, 2)

// метод возвращает удаленные значения
console.log(deletedColors)  // ['blue', 'red']
// исходный массив изменяется
console.log(colors)         // ['yellow', 'green']
```

Если после второго параметра указать через запятую значения — они будут вставлены в массив.
```js
const colors = ['blue', 'red', 'yellow', 'green']

colors.splice(2, 0, 'pink', 'purple')

console.log(colors)  // ['blue', 'red', 'pink', 'purple', 'yellow', 'green']
```

--- 

<div align="center">

### Методы доступа

</div>

---

Нижеприведенные методы не изменяют исходный массив.

---

Метод slice(start, stop) — возвращает копию массива от индекса start до индекса stop.

---

<div align="center">

### Методы обхода

</div>

---

Метод forEach() — выполняет переданную функцию для каждого элемента массива.

---

Метод map() — выполняет переданную функцию для каждого элемента массива, 




---

С остальными методами массива можно ознакомиться на MDN:
[https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array)

---

Источники:
* [`push()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
* [`pop()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)
* [`unshift()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift)
* [`shift()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/shift)
* [`reverse()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse)
* [`splice()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
* [`slice()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
* [`forEach()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
* [`map()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
* [`every()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
* [`some()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
* [`filter()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
* [`reduce()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)
* [`indexOf()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)
* [`lastIndexOf()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/lastIndexOf)
* [`concat()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)
* [`join()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
* [`toString()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/toString)









