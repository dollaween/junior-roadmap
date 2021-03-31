<div align="center">

# Тесты: Number

[Главная](https://github.com/dollaween/junior-roadmap/)
|
[Карта](/roadmap/README.md)
|
[Тесты](/tests/README.md)
|
[Задачи](/tasks/README.md)

</div>

---

##### 1. Какой будет вывод?

```javascript
let x = 10
let y = 5
let z = 3
console.log((x + y) / z)
```

1. `10`
2. `5`
3. `3`
4. `0`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
let x = 5
let y = 2
console.log(x ** y)
```

1. `5`
2. `10`
3. `25`
4. `32`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Оператор `**` возводит левый операнд в степень равную правому операнду.

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
let x = 10
let y = 3
console.log(x % y)
```

1. `0`
2. `1`
3. `3`
4. `10`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Оператор деления по модулю `%` отдает остаток после деления числа `x` на `y`.

`10` делится на `3` три раза и остается остаток от деления `1`.

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
const x = 10
console.log(x.toFixed(2))
```

1. `10`
2. `10.0`
3. `10.00`
4. `10.10`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Метод `toFixed()` форматирует число приводя его к указанному количеству знаков после запятой

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
const x = 10.1234567
console.log(x.toFixed(5))
```

1. `10.12345`
2. `10.12346`
3. `10.12344`
4. `10`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Метод `toFixed()` форматирует число приводя его к указанному количеству знаков после запятой с округлением.

</p>
</details>


