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

console.log(deleted)  // 'reviewer'
console.log(roles)    // ['admin', 'moderator']
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

Метод `indexOf()` — возвращает первый индекс, по которому данный элемент может быть найден в массиве или -1, если такого индекса нет.

```js
const calendar = ['Янв', 'Фев', 'Март', 'Янв', 'Фев', 'Март']

const index1 = calendar.indexOf('Март')
const index2 = calendar.indexOf('Дек')

console.log(index1)  // 2
console.log(index2)  // -1
```

Вторым аргументом можно указать индекс, откуда будет начинаться поиск:

```js
const calendar = ['Янв', 'Фев', 'Март', 'Янв', 'Фев', 'Март']

console.log(calendar.indexOf('Март', 3))  // 5
```

---

Метод `lastIndexOf()` — возвращает первый индекс, по которому данный элемент может быть найден в массиве или -1, если такого индекса нет.

```js
const calendar = ['Янв', 'Фев', 'Март', 'Янв', 'Фев', 'Март']

const index1 = calendar.lastIndexOf('Март')
const index2 = calendar.lastIndexOf('Дек')

console.log(index1)  // 5
console.log(index2)  // -1
```

---

Метод `slice(start, stop)` — возвращает копию массива от индекса `start` до индекса `stop` (не включительно).

```js
const fruits = ['apple', 'orange', 'pear', 'banana']

const result = fruits.slice(1, 3)

console.log(result)  // ['orange', 'pear']
```

---

Метод `concat()` — соединяет массив, на котором был вызван с заданным массивом и возвращает получившийся объединенный массив.

```js
const searchSites = ['google.com', 'yahoo.com']
const socialNetworks = ['facebook.com', 'instagram.com']

const sites = searchSites.concat(socialNetworks)

console.log(sites)  // ['google.com', 'yahoo.com', 'facebook.com', 'instagram.com']
```

---

Метод `join(separator)` — объединяет все элементы массива в строку.

Если указать `separator` — то он будет вставлен в строку между элементами.

```js
const strings = ['I', 'will', 'be', 'back']

const example1 = strings.join()
const example2 = strings.join(' ')
const example3 = strings.join('-')

console.log(example1)  // 'I,will,be,back'
console.log(example2)  // 'I will be back'
console.log(example3)  // 'I-will-be-back'
```

---

Метод `toString()` — объединяет все элементы массива в строку. Метод работает так же, как и `join()`, но отсутствует передаваемый параметр.

```js
const elems = ['Янв', true, { name: 123 }, 66]

const str = elems.toString()

console.log(str)  // 'Янв,true,[object Object],66'
```

---

<div align="center">

### Методы обхода

</div>

---

Метод `forEach()` — выполняет указанную функцию для каждого элемента массива.

```js
const fighters = ['Jax', 'Johnny', 'Liu']

fighters.forEach((element) => {
  console.log(element)
})
```

---

Метод `map()` — создает новый массив, выполняет переданную функцию для каждого элемента массива и заполняет результатами созданный массив.

В переданной функции значение должно быть возвращено с помощью ключевого слова `return`, иначе новый массив будет забит элементами `undefined`.

```js
const alphabet = ['abc', 'def', 'jhi']

const upperAlphabet = alphabet.map((element) => {
  return element.toUpperCase()
})

console.log(upperAlphabet)  // ['ABC', 'DEF', 'JHI']
```

---

Метод `every()` — проверяет, удовлетворяют ли все элементы массива условию, заданному в передаваемой функции.

```js
const balances = [150, 70, 100]

// Пример 1
let result = balances.every((balance) => {
  return balance > 50
})

console.log(result)  // true

// Пример 2
result = balances.every((balance) => balance > 100)

console.log(result)  // false
```

---

Метод `some()` — проверяет, удовлетворяет ли какой-либо элемент массива условию, заданному в передаваемой функции.

```js
const names = ['John', 'Michael', 'Ethan']

// Пример 1
let result = names.some((name) => {
  return name.length > 6
})

console.log(result)  // true

// Пример 2
result = names.some((name) => name.length > 14)

console.log(result)  // false
```

---

Метод `filter()` — создает новый массив со всеми элементами, удовлетворяющими условию в передаваемой функции.

```js
const ages = [25, 16, 23, 44, 31]

const acceptedAges = ages.filter((age) => {
  return age >= 25
})

console.log(acceptedAges)  // [25, 44, 31]
```

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









