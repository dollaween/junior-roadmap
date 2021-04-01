<div align="center">

## Задачи
# Математические операции

[Главная](https://github.com/dollaween/junior-roadmap/)
|
[Карта](/roadmap/README.md)
|
[Тесты](/tests/README.md)
|
[Задачи](/tasks/README.md)

</div>

---

##### 1. Сложение

Даны три числа `10`, `5` и `2`. Для каждого числа создайте переменную и выведите в консоль результат их сложения.

```js
console.log(/* ... */)
// 17
```

<details><summary><b>Решение</b></summary>
<p>

```js
const a = 10
const b = 5
const c = 2

console.log(a + b + c)
```

</p>
</details>

---

##### 2. Вычитание и возведение в степень

Даны три числа `3`, `5`, `12`. Для каждого числа создайте переменную. Вычтите из числа `5` число `3`, а затем возведите результат в степень `12`.

```javascript
console.log(/* ... */)
// 4096
```

<details><summary><b>Решение</b></summary>
<p>

```js
const a = 3
const b = 5
const c = 12

console.log((b - a) ** c)
```

</p>
</details>

---

##### 3.

Даны два числа `1.23` и `4.56`. Для каждого числа создайте переменную. Умножьте первое число на второе. Выведите в консоль результат перемножения чисел с точностью до двух знаков после запятой.

```js
console.log(/* ... */)
// 5.61
```

<details><summary><b>Подсказка</b></summary>
<p>

Для приведения числа к определенному количеству знаков после запятой используйте метод `toFixed()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const a = 1.23
const b = 4.56
const c = a * b

console.log(c.toFixed(2))
```

</p>
</details>

