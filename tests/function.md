<div align="center">

# Тесты: Функции

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

##### 1. Какой будет вывод?

```javascript
function subtraction(a, b) {
  a - b
}

console.log(subtraction(45, 10))
```

1. `undefined`
2. `35`
3. `'35 - 10'`
4. `null`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Функция `subtraction()` ничего не возвращает. Если отсутствует возвращение значения с помощью оператора `return`, то функция в конце своей работы вернет значение `undefined`.

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
function getString(a, b, c) {
  return a
  return b
  return c
}

getString('Maximum', 'Binary', 'Tree')
```

1. `'Maximum'`
2. `'Binary'`
3. `'Tree'`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Оператор `return` — завершает выполнение функции и возвращает значение. Данная функция всегда будет возвращать значение параметра `a`.

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
function showWarning(error) {
  if (error) {
    return 'Got error'
  }
  
  return 'System error'
}

console.log(showWarning(''))
```

1. `'Got error'`, `'System error'`
2. `'Got error'`
3. `'System error'`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

В условии `if (error)` мы имеем следующие преобразования:

`if (error)` -> `if ('')` -> `if (false)`

Инструкция внутри `if` не будет выполнена, потому что условие ложно.

Значит, функция дойдет до следующего оператора `return` и вернет `'System error'`.

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
function showSide(side = 'Alliance') {
  console.log(side)
}

showSide('Empire')
```

1. `'Alliance'`
2. `'Empire'`
3. `NaN`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Через оператор присваивание `=` в параметрах функции мы переопределяем значение по-умолчанию. Значение по-умолчанию устанавливается, если функция не получает нужного параметра.

В данном примере, мы передаем в функцию значение `'Empire'` для параметра `side`, поэтому значение `'Alliance'` будет проигнорировано.

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
function division(a, b = 1, c) {
  console.log(a / b / c)
}

division(16, 2)
```

1. `16`
2. `8`
3. `Infinity`
4. `NaN`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

При вызове функции, мы имеем следующие параметры:
* `a` === `16`
* `b` === `2`
* `c` === `undefined`

Так как параметр `c` не получает никакого значения, то по-умолчанию, его значение будет установлено в `undefined`.

В результате операции `16 / 2 / undefined` мы получаем `NaN`.

</p>
</details>

















