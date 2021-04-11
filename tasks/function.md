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

Напишите функцию, которая возвращает косинус числа.

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

