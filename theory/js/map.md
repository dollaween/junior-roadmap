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

**Map** — это коллекция пар ключ/значение (как и объект).

Отличия Map от Object:
- В качестве ключа в Map можно использовать любые типы данных (в объекте в качестве ключа могут быть только строки или числа).
- Map запоминает порядок вставки (объект — сортирует).

```js
const map = new Map()

map.set('name', 'John')
console.log(map.get('name'))  // 'John'
```

Свойства и методы:
- `new Map()` – создаёт коллекцию.
- `map.set(key, value)` – записывает по ключу key значение value.
- `map.get(key)` – возвращает значение по ключу или undefined, если ключ key отсутствует.
- `map.has(key)` – возвращает true, если ключ key присутствует в коллекции, иначе false.
- `map.delete(key)` – удаляет элемент по ключу key.
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

Источники:
- [Map и Set](https://learn.javascript.ru/map-set)
- [ECMAScript: Map](https://tc39.es/ecma262/#sec-map-objects)
- [MDN: Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
