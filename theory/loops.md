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

***С помощью неверно составленного цикла можно заставить браузер зависнуть!*** Убедитесь, что условие выхода написано верно и является достижимым.

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

Цикл `while` — выполняет действия, пока условие истинно.

```js
while ([условие]) {
  [действия]
}
```

Пример:

```js
let i = 0

while (i < 3) {
  i++
  console.log(i)
}

// 1
// 2
// 3
```

---

Оператор `break` — прерываем цикл.

```js
for (let i = 0; i < 10; i++) {
  if (i === 3) {
    break
  }
  console.log(i)
}

// 0
// 1
// 2
```

---

Оператор `continue` — прерывает текущую итерацию цикла и переходит к следующей.

```js
// выводим только четные числа, прерывая выполнение итерации, если число нечетное

for (let i = 0; i < 9; i++) {
  if (i % 2) {
    continue
  }
  console.log(i)
}

// 0
// 2
// 4
// 6
// 8
```

---

Источники:
* [Циклы и итерации](https://developer.mozilla.org/ru/docs/Web/JavaScript/Guide/Loops_and_iteration)
