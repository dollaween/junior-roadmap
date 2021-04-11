<div align="center">

# Функции

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

##### 1. Сложение

Напишите функцию, которая возвращает результат сложения трех чисел.

```js
function sum() {
  /* ... */
}

console.log(sum(1, 2, 3))
// 6
```

<details><summary><b>Решение</b></summary>
<p>

```js

function sum(a, b, c) {
  return a + b + c
}

sum(1, 2, 3)
```

</p>
</details>

---

##### 2. Косинус числа

Напишите функцию, которая возвращает косинус числа. Если в функцию передано не число — верните `NaN`.

```js
function cos() {
  /* ... */
}

console.log(cos(1))
// 0.5403023058681398
```

<details><summary><b>Подсказка</b></summary>
<p>

Для вычисления косинуса числа, используйте метод `Math.cos()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
function cos(num) {
  return Math.cos(num)
}

cos(1)
```

</p>
</details>

---

##### 3. Проверка типов

Напишите функцию, которая будет проверять тип входного параметра:
* Если передано число — возвращает `'Это число'`.
* Если передана строка — возвращает `'Это строка'`.
* Если передан boolean — возвращает `'Это логическое значение'`.
* Если передан NaN — возвращает `'Это не число'`.
* Во всех остальных случаях — возвращает `'Тип не определен'`

```js
function checkType() {
  /* ... */
}

console.log(checkType(10))
// 'Это число'

console.log(checkType('Hello'))
// 'Это строка'

console.log(checkType(true))
// 'Это логическое значение'

console.log(checkType(NaN))
// 'Это не число'

console.log(checkType([1, 2, 3]))
// 'Тип не определен'
```

<details><summary><b>Подсказка</b></summary>
<p>

Для определения типа элемента, используйте оператор `typeof`.

Для определения типа `NaN`, используйте функцию `isNaN()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
function checkType() {
  const type = typeof elem

  switch (type) {
    case 'string':
      return 'Это строка'
    case 'boolean':
      return 'Это логическое значение'
    case 'number':
      if (isNaN(elem)) {
        return 'Это не число'
      }
      return 'Это число'
    default:
      return 'Тип не определен'
  }
}

checkType(10)
```

</p>
</details>


