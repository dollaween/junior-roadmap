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

