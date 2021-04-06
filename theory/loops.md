<div align="center">

# Циклы

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

Циклы — простой способ сделать какое-либо действие несколько раз.

Существует несколько циклов, но все они делают одно и то же: `for`, `do ... while`, `while`.

**С помощью неверного цикла можно заставить браузер зависнуть!** Убедитесь, что условие выхода написано верно и является достижимым.

---

Цикл `for` — повторяет действие, пока не произойдет событие завершения цикла.

```js
for ([начало]; [условие]; [шаг]) {
  [действия]
}
```

Пример:
```js
for (let i = 0; i < 5; i++) {
  console.log(i)
}
// 0
// 1
// 2
// 3
// 4
```

С помощью циклов можно итерировать массивы, строки, объекты:
```js
const countries = ['Russia', 'Ukraine', 'Kazakhstan']

for (let i = 0; i < countries.length; i++) {
  console.log(countries[i])
}
// 'Russia'
// 'Ukraine'
// 'Kazakhstan'
```


---

Источники:
* [Циклы и итерации](https://developer.mozilla.org/ru/docs/Web/JavaScript/Guide/Loops_and_iteration)
