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

---

##### 5. Какой будет вывод?

```javascript
console.log('Country Music'.toLowerCase())
```

1. `COUNTRY MUSIC`
2. `Country Music`
3. `Country music`
4. `country music`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Метод `toLowerCase()` возвращает значение строки, преобразованное в нижний регистр.

</p>
</details>

---

##### 6. Какой будет вывод?

```javascript
console.log('Country Music'.toUpperCase())
```

1. `COUNTRY MUSIC`
2. `Country Music`
3. `Country music`
4. `country music`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `toUpperCase()` возвращает значение строки, преобразованное в верхний регистр.

</p>
</details>

---

##### 7. Какой будет вывод?

```javascript
const place = 'Cinema'
console.log(place.trim())
```

1. `CINEMA`
2. `Cinema`
3. `cinema`
4. `null`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Метод `trim()` удаляет пробельные символы с начала и конца строки.

Примеры:
* `'   Cinema'.trim()` —> `Cinema`
* `'Cinema    '.trim()` —> `Cinema`
* `'   Cinema  '.trim()` —> `Cinema`

</p>
</details>

---

##### 8. Какой будет вывод?

```javascript
const myAge = 'My age is 20'
console.log(myAge.replace('20', '21'))
```

1. `My age is 20`
2. `My age is 21`
3. `My age is`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Метод `replace()` возвращает новую строку с заменой первого параметра на второй.

Примеры:
* `'My age is 20'.replace('My', 'His')` -> `His age is 20`
* `'My age is 20'.replace('My age is 20', 'I\'m too old')` -> `I'm too old`

</p>
</details>

---

##### 9. Какой будет вывод?

```javascript
const app = 'TikTok'
console.log(app.slice(2))
```

1. `Ti`
2. `ikTok`
3. `kTok`
4. `Tok`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Метод `slice()` возвращает новую строку, начинающуюся по индексу от первого параметра, заканчивающуюся по индексу второго параметра.

Если второй параметр не указан — будет возвращена строка, начинающаяся с индекса первого параметра и до конца.

Если параметр отрицательный — то отсчет будет идти с конца.

Примеры:
* `'TikTok'.slice(3, 6)` -> `Tok`
* `'TikTok'.slice(3, 8)` -> `Tok`
* `'TikTok'.slice(3)` -> `Tok`
* `'TikTok'.slice(-3)` -> `Tok`

</p>
</details>

---

##### 10. Какой будет вывод?

```javascript
console.log('TikTok'.slice(-2))
```

1. ``
2. `Tok`
3. `ok`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Если параметр отрицательный — то отсчет будет идти с конца.

</p>
</details>

