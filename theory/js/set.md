<div align="center">

# Set

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

**Объект Set** — это коллекция, состоящая из уникальных значений (и без ключей).
  
Особенности `Set`:
- Коллекция состоит только из уникальных значений.
- Коллекция запоминает порядок добавления значений.

Свойства и методы:
- `new Set(iterable)` — создает `Set`, и, если в качестве аргумента был предоставлен итерируемый объект, то копирует его значения в новый `Set`.
- `set.add(value)` — добавляет значение (если такое значение уже есть, то ничего не делает), возвращает тот же объект `set`.
- `set.delete(value)` — удаляет значение, возвращает `true` (если произошло удаление) или `false` (если такого значения уже не было).
- `set.has(value)` — возвращает `true`, если значение присутствует в коллекции, иначе `false`.
- `set.clear()` — удаляет все имеющиеся значения.
- `set.size` — возвращает количество элементов в коллекции.

Пример:
```js
const character1 = 'Aragorn'
const character2 = 'Frodo'
const character3 = 'Gandalf'

const set = new Set()

set.add(character1)
set.add(character1)
set.add(character2)
set.add(character3)
set.add(character2)
set.add(character1)

// Повторяющиеся значения не будут записаны в Set еще раз, поэтому с помощью свойства size мы можем узнать количество уникальных значений в коллекции
console.log(set.size)
// 3
```

---

<div align="center">

### Перебор объекта Set

</div>

---

Для перебора значений `Set` можно использовать следующие способы:
- `set.forEach()` — итерирует коллекцию по значению.
- `for ... of` — цикл для итерирования коллекции по значению.
- `set.values()` — возвращает итерируемый объект по значениям.

Методы, которые присутствуют для обратной совместимости с `Map`:
- `set.keys()` — то же самое, что и `set.values()`.
- `set.entries()` — возвращает итерируемый объект вида `[значение, значение]`.

Пример:
```js
const set = new Set(['Aragorn', `Frodo`, `Gandalf`])

for (let character of set) {
  console.log(character)
}

set.forEach((value, valueAgain, set) => {
  console.log(value)
})

// В обоих вариантах вывод следующий:
// Aragorn
// Frodo
// Gandalf
```




---

Источники:
- [Map и Set](https://learn.javascript.ru/map-set)

