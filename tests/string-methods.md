<div align="center">

# Тесты: Методы строки

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
const phrase = 'Winter is coming'
console.log(phrase.charAt(1))
```

1. `W`
2. `i`
3. `undefined`
4. `null`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Метод `charAt()` — возвращает указанный символ строки. Счет начинается от `0`. То есть `charAt(0)` — `W`, `charAt(1)` — `i`.

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
console.log('Winter is coming'.includes('is'))
```

1. `Winter is coming`
2. `is`
3. `7`
4. `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Метод `includes()` проверяет, содержит ли строка заданную подстроку, и возвращает, соответственно `true` или `false`.

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
console.log(`Winter is coming`.startsWith('is'))
```

1. `Winter`
2. `7`
3. `true`
4. `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Метод `startsWith()` помогает определить, начинается ли строка с символов указанных в скобках, возвращая, соответственно, `true` или `false`.

Примеры:
* `'Winter is coming'.startsWith('Winter')` —> `true`
* `'Winter is coming'.startsWith('coming')` —> `false`

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
let title = 'Hookah place'
title = 'Hookah space'
console.log(title.endsWith('space'))
```

1. `true`
2. `false`
3. `place`
4. `space`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `endsWith()` позволяет определить, заканчивается ли строка символами указанными в скобках, возвращая, соответственно, `true` или `false`.

</p>
</details>

