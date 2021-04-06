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

Объект — это набор свойств, состоящих из пары 'ключ: значение'.

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

const house = {
  city: 'New York',
  address: 'central street, 15',
  rooms: 4,
  hasBathroom: true,
  cost: '4 000 000$'
}

// если в названии ключа есть пробелы, то его можно записать так:
const planet = {
  name: 'Mars',
  ['Солнечная система?']: true,
  ['Can be reached']: true
}
```

---

Источники:
* [Работа с объектами](https://developer.mozilla.org/ru/docs/Web/JavaScript/Guide/Working_with_Objects)


