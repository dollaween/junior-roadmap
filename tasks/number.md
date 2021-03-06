<div align="center">

## Задачи
# Математические операции

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

##### 3. Умножение и форматирование числа

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

---

##### 4. Деление по модулю и округление в большую сторону

Даны два числа `100` и `31`. Используя деление по модулю разделите `100` на `31`. Разделите остаток от деления по модулю на `2` и выведите в консоль полученное число с округлением до ближайшего целого в большую сторону.

```js
console.log(/* ... */)
// 4
```

<details><summary><b>Подсказка</b></summary>
<p>

Для деления по модулю используйте оператор `%`.

Для округления в большую сторону используйте метод `Math.ceil()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const a = 100
const b = 31
const c = (100 % 31) / 2

console.log(Math.ceil(c))
```

</p>
</details>

---

##### 5. Самое большое и самое маленькое числа

Даны числа `4`, `2`, `6` и `5`. Используя методы объекта `Math` выведите в консоль сперва самое большое число, а затем самое маленькое число.

```js
console.log(/* ... */)
// 6

console.log(/* ... */)
// 2
```

<details><summary><b>Подсказка</b></summary>
<p>

Для определения самого большого числа используйте метод `Math.max()`.

Для определения самого маленького числа используйте метод `Math.min()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const a = 4
const b = 2
const c = 6
const d = 5

console.log(Math.max(a, b, c, d))
console.log(Math.min(a, b, c, d))
```

</p>
</details>

---

##### 6. Случайное число

Выведите в консоль случайное число от 0 до 100 (не включительно).

```js
console.log(/* ... */)
// Случайное число от 0 до 100
```

<details><summary><b>Подсказка</b></summary>
<p>

Для генерирования случайного числа используйте метод `Math.random()`.

Для округления числа до целого в меньшую сторону используйте метод `Math.floor()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
console.log(Math.floor(Math.random() * 100))
```

</p>
</details>


