<div align="center">

# Список тестов

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
console.log(title)
let title = 'Star Wars'
```

1. `'Star Wars'`
2. `undefined`
3. `null`
4. `ReferenceError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

На момент вывода `title` в `console.log()` переменной еще не присвоено никакое значение, даже `undefined`.

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
console.log(title)
var title = 'Big Bang Theory'
```

1. `'Big Bang Theory'`
2. `undefined`
3. `null`
4. `ReferenceError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Объявление переменной через ключевое слово `var` отличается от объявления переменной через ключевое слово `let`:
- `var` — объявляет переменную и присваивает ей undefined.
- `let` — только объявляет переменную.

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
console.log(title)
const title = 'Warcraft'
```

1. `Warcraft`
2. `undefined`
3. `null`
4. `ReferenceError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Объявление переменной через ключевое слово `const` аналогично объявлению переменной через ключевое слово `let`.

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
let age = 25
age = 26
console.log(age)
```

1. `25`
2. `26`
3. `undefined`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Значение переменных, объявленных через `let`, можно изменять.

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
let age = 25
let age = 26
console.log(age)
```

1. `25`
2. `26`
3. `undefined`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

В памяти уже существует переменная с идентификатором `age`. Поэтому повторное объявление переменной вызовет ошибку `SyntaxError`.

</p>
</details>

