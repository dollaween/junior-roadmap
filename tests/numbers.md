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

**Ответ: 2**

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

Метод `toFixed()` форматирует число приводя его к указанному количеству знаков после запятой.

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

---

##### 6. Какой будет вывод?

```javascript
const x = -12.345
console.log(Math.floor(x))
```

1. `-11`
2. `-12`
3. `-13`
4. `-12.3`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Метод `Math.floor()` — округляет число до ближайшего меньшего целого.

</p>
</details>

---

##### 7. Какой будет вывод?

```javascript
const x = 12.345
console.log(Math.ceil(x))
```

1. `11`
2. `12`
3. `13`
4. `12.4`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Метод `Math.ceil()` — округляет число до ближайшего большего целого.

</p>
</details>

---

##### 8. Какой будет вывод?

```javascript
const x = -12.345
console.log(Math.round(x))
```

1. `-11`
2. `-12`
3. `-13`
4. `12`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Метод `Math.round()` — округляет число к ближайшему целому.

</p>
</details>


---

##### 9. Какой будет вывод?

```javascript
const x = -12.345
console.log(Math.abs(x))
```

1. `-11`
2. `-12.345`
3. `-13`
4. `12.345`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Метод `Math.abs()` — возвращает абсолютное значение числа.

</p>
</details>

---

##### 10. Какой будет вывод?

```javascript
const x = 10
const y = 5
console.log(Math.max(x, y))
```

1. `10`
2. `5`
3. `10, 5`
4. `50`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `Math.max()` — возвращает наибольший из аргументов.

</p>
</details>

---

##### 11. Какой будет вывод?

```javascript
const x = 10
const y = 5
const z = 2
console.log(Math.min(x, y, z))
```

1. `10`
2. `5`
3. `2`
4. `0`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Метод `Math.min()` — возвращает наименьший из аргументов.

</p>
</details>

---

##### 12. Какой будет вывод?

```javascript
const x = 10
console.log(x > Math.random())
```

1. `true`
2. `false`
3. `10`
4. `0`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `Math.random()` — возвращает псевдослучайное число с плавающей запятой от 0 (включительно) до 1 (но не включительно).

</p>
</details>

---

##### 13. Какой из вариантов возвращает целое число от 0 до 99 (включительно)?

```javascript
// 1
Math.random()

// 2
Math.floor(Math.random())

// 3
Math.floor(Math.random() * 100)

// 4
Math.floor(Math.random() * 100) + 1
```

1. `1`
2. `2`
3. `3`
4. `4`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

</p>
</details>





