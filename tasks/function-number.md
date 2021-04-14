<div align="center">

# Работа с числами

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

##### 1. Сложение двух чисел

Напишите функцию, которая принимает два числа и возвращает результат их сложения.  
Также функция должна вывести результат сложения в консоль.

```js
function sum() { /* ... */ }

sum(10, 5)  // 15
sum(7, 16)  // 23
```

<details><summary><b>Решение</b></summary>
<p>

```js
function sum(a, b) {
  const result = a + b
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 2. Деление трех чисел

Напишите функцию, которая принимает три числа и возвращает результат их деления (число 1 / число 2 / число 3).  
Также функция должна вывести результат деления в консоль.

```js
function division() { /* ... */ }

division(10, 5, 2)   // 1
division(100, 2, 2)  // 25
```

<details><summary><b>Решение</b></summary>
<p>

```js
function division(a, b, c) {
  const result = a / b / c
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 3. Перемножение чисел

Напишите функцию, которая будет принимать четыре числа и возвращать результат их перемножения. Сделайте так, чтобы результат не становился `NaN`, если передать не все параметры.  
Также функция должна вывести результат перемножения в консоль.

```js
function mult() { /* ... */ }

mult(1, 2, 3, 4)   // 24
mult(6, 3, 17, 5)  // 1530
mult(10, 2)        // 20
mult(1)            // 1
mult()             // 0
```

<details><summary><b>Решение</b></summary>
<p>

```js
function mult(a = 0, b = 1, c = 1, d = 1) {
  const result = a * b * c * d
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 4. Возвращение косинуса

Напишите функцию, которая принимает число и возвращает косинус переданного числа.  
Также функция должна вывести результат в консоль.

```js
function cos() { /* ... */ }

cos(1)    // 0.5403023058681398
cos(0.5)  // 0.8775825618903728
```

<details><summary><b>Решение</b></summary>
<p>

```js
function cos(num) {
  const result = Math.cos(num)
  console.log(result)
  return result
}
```

</p>
</details>













