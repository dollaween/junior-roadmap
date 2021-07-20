<div align="center">

# Map

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

**Map** — это коллекция пар ключ/значение. Map похож на объект, но имеет собственные свойства и методы, а также некоторые отличия.

Отличия Map от Object:
- В качестве ключа в Map можно использовать любые типы данных. В объекте в качестве ключа могут быть только строки, числа или символы.
- Map запоминает порядок добавления элементов, объект — нет.
- У Map доступно свойство `size`, которое позволяет получить количество элементов в коллекции. Количество элементов в объекте может быть подсчитано только с помощью дополнительных операций.
- Производительность Map выше в сценариях частого добавления/удаления пар `ключ/значение`.
- Map нативно не поддерживает сериализацию в JSON, объект — поддерживает.

```js
const map = new Map()

map.set('name', 'John')
console.log(map.get('name'))  // 'John'
```

Свойства и методы:
- `new Map()` – создаёт коллекцию.
- `map.set(key, value)` – записывает по ключу `key` значение `value`.
- `map.get(key)` – возвращает значение по ключу или `undefined`, если ключ `key` отсутствует.
- `map.has(key)` – возвращает `true`, если ключ `key` присутствует в коллекции, иначе `false`.
- `map.delete(key)` – удаляет элемент по ключу `key`.
- `map.clear()` – очищает коллекцию от всех элементов.
- `map.size` – возвращает текущее количество элементов.

Пример с ключом-объектом:
```js
const person = {
  name: 'John',
  age: 33
}

const house = {
  city: 'Moscow',
  street: 'Lefortovo Tunnel'
}

const owners = new Map()
owners.set(house, person)

console.log(owners.get(house))
// { name: 'John', age: 33 }
```

---

<div align="center">

### Перебор ключей и значений

</div>

---

Для перебора коллекции Map есть 4 метода:
- `map.keys()` – возвращает итерируемый объект по ключам.
- `map.values()` – возвращает итерируемый объект по значениям.
- `map.entries()` – возвращает итерируемый объект по парам вида `[ключ, значение]`, этот вариант используется по умолчанию в `for..of`.
- `map.forEach()` – итерирует коллекцию.

```js
const map = new Map([
  ['04:17': 'sunrise'],
  ['20:57': 'sunset']
])

for (let key of map.keys()) {
  console.log(key)
}
// '04:17'
// '20:57'

for (let value of map.values()) {
  console.log(value)
}
// 'sunrise'
// 'sunset'

for (let item of map) {
  console.log(item)
}
// ['04:17', 'sunrise']
// ['20:57', 'sunset']

map.forEach((value, key, map) => {
  console.log(`${key} – ${value}`)
})
// '04:17 – sunrise'
// '20:57 – sunset'

```

---

<div align="center">

### Преобразование в Map

</div>

---

Из массива:
```js
const arr = [
  ['04:17', 'sunrise'],
  ['20:57', 'sunset']
]

const map = new Map(arr)
```

Из объекта:
```js
const obj = {
  name: 'Sam',
  age: 24
}

const map = new Map(Object.entries(obj))
```

---

<div align="center">

### Преобразование из Map

</div>

---

В массив:
```js
const map = new Map([
  ['04:17', 'sunrise'],
  ['20:57', 'sunset']
])

const arr1 = [...map]
const arr2 = Array.from(map)
const arr3 = Array.from(map, ([key, value]) => [key, value])
```

В объект:
```js
const map = new Map([
  ['04:17', 'sunrise'],
  ['20:57', 'sunset']
])

const obj = Object.fromEntries(map)
```


---

Источники:
- [Map и Set](https://learn.javascript.ru/map-set)
- [ECMAScript: Map](https://tc39.es/ecma262/#sec-map-objects)
- [MDN: Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
