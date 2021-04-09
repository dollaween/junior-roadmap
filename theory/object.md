<div align="center">

# Объекты

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

Объект — это набор свойств, состоящих из пары `'ключ': 'значение'`.

```js
const obj = {
  'ключ': 'значение'
}
```

Примеры:
```js
const person = {
  name: 'John',
  age: 33,
  isWorking: true
}

// если в названии ключа есть пробелы, то его можно записать в виде строки:
const planet = {
  name: 'Mars',
  'Солнечная система?': true,
  'Can be reached': true
}

// в объекте могут содержаться любые типы данных, включая и другие объекты:
const house = {
  city: 'New York',
  address: 'central street, 15',
  rooms: ['kitchen', 'bedroom'],
  hasBathroom: true,
  cost: 4000000,
  owner: person
}
```

Получить значение объекта можно двумя способами:
1. Обратиться к свойству объекта через точку
2. Обратиться к свойству объекта через квадратные скобки

```js
const phone = {
  company: 'Apple',
  model: 'iPhone XR',
  'year of issue': 2018
}

console.log(phone.company)
// 'Apple'

// при обращении через квадратные скобки свойство должно быть строкой
console.log(phone['model'])
// 'iPhone XR'

// если в названии ключа есть пробелы, то единственный способ получить значение — обращение через квадратные скобки
console.log(phone['year of issue'])
// 2018
```

В объекте содержатся только уникальные ключи. Если записать несколько одинаковых ключей — последний перезатрет все предыдущие:

```js
const plant = {
  title: 'Кактус',
  title: 'Роза'
}

console.log(plant)
// { title: 'Роза' }

console.log(plant.title)
// 'Роза'
```

---

<div align="center">

### Методы объектов

</div>

---

Метод `Object.keys()` — возвращает массив свойств объекта.

```js
const planet = {
  title: 'Earth',
  radius: 6371,
  hasLife: true
}

const keys = Object.keys(planet)

console.log(keys)
// ['title', 'radius', 'hasLife']
```

---

Метод `Object.values()` — возвращает массив значений объекта.

```js
const dates = {
  'Крещение Руси': 998,
  'Невская битва': 1240,
  'Полтавская битва': 1709
}

const values = Object.values(dates)

console.log(values)
// [998, 1240, 1709]
```

---

Метод `Object.entries()` — возвращает массив, содержащий пары `'ключ': 'значение'` в виде `['ключ', 'значение']`.

```js
const coordinates = {
  x: 10,
  y: 22,
  z: 3
}

const entries = Object.entries(coordinates)

console.log(entries)
// [['x', 10], ['y', 22], ['z', 3]]
```

---

Источники:
* [Работа с объектами](https://developer.mozilla.org/ru/docs/Web/JavaScript/Guide/Working_with_Objects)

















