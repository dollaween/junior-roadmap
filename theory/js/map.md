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

Главное отличие Map от Object — в качестве ключа в Map можно использовать любые типы данных (в объекте в качестве ключа могут быть только строки или числа).

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
