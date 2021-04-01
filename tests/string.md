<div align="center">

# Тесты: String, кавычки, конкатенация, методы

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
const city = 'Москва'
const address = 'Ленинский проспект'
const house = '10А'
console.log(city + address + house)
```

1. `Москва Ленинский проспект 10А`
2. `МоскваЛенинский проспект10А`
3. `Москва, Ленинский проспект, 10А`
4. `Москва`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Конкатенация (объединение) строк происходит без добавления символов движком "от себя" — если между строками не было пробелов или запятых — то и в итоговой строке их не будет.

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
const address = 'Профсоюзная'
const house = 120
console.log(address + house)
```

1. `Профсоюзная120`
2. `Профсоюзная 120`
3. `Профсоюзная, 120`
4. `TypeError: строки и числа складывать нельзя!`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Строки и числа можно конкатенировать (объединять). В результате конкатенации мы получим строку.

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
const firstName = 'Jon'
const lastName = "Snow"
console.log(firstName + ' ' + lastName)
```

1. `TypeError: строки с разными кавычками складывать нельзя!`
2. `Jon Snow`
3. `JonSnow`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Одинарные и двойные кавычки ничем не отличаются и их можно конкатенировать.

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
const lastName = 'Snow'
console.log('Jon lastName')
```

1. `Jon lastName`
2. `Jon Snow`
3. `JonSnow`
4. `Jon undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Символы в одинарных и двойных кавычках являются обычным текстом. Исключение составляет только символ обратного слэша `\`.

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
const x = '10'
const y = 5
console.log(x + y)
```

1. `15`
2. `10`
3. `5`
4. `105`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

При конкатенации, если один из операндов является строкой, то оба операнда будут приведены к строке и будут конкатенироваться как строки.

</p>
</details>

---

##### 6. Какой будет вывод?

```javascript
const color = 'grey'
console.log(`Wolf is ${color}`)
```

1. `Wolf is grey`
2. `Wolf is ${color}`
3. `Wolf is color`
4. `TypeError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

В апострофах (обратных кавычках) можно использовать переменные, если обернуть их в конструкцию `${}`.

</p>
</details>

---

##### 7. Какой будет вывод?

```javascript
const color = 'red'
console.log("Fox is ${color}")
```

1. `Fox is red`
2. `Fox is ${color}`
3. `Fox is red`
4. `TypeError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Символы в одинарных и двойных кавычках являются обычным текстом. Исключение составляет только символ обратного слэша `\`.

</p>
</details>

---

##### 8. Какой будет вывод?

```javascript
const city = 'Санкт-Петербург'
const street = "Рубинштейна"
const house = `10`
console.log(city + ' ' + street + ' ' + house)
```

1. `Санкт-Петербург Рубиншейна house`
2. `TypeError`
3. `Санкт-Петербург Рубинштейна 10`
4. `city street 10`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Конкатенировать строки в одинарных, обратных кавычках и апострофах можно.

</p>
</details>

---

##### 9. Какой будет вывод?

```javascript
console.log('\u00A9')
```

1. `\t`
2. ` `
3. `&nbsp;`
4. `    `

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Символ обратного слэша `\` является служебным. В данном случае, `\t` — это табуляция.

</p>
</details>


