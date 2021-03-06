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

---

##### 6. Какой будет вывод?

```javascript
const fn = function(a, ...params) {
  console.log(params)
}

fn(true, false, false)
```

1. `'false', 'false'`
2. `[true, false, false]`
3. `[false, false]`
4. `Error: fn — не функция`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

**Оставшиеся параметры** `...params` — вбирают в себя все передаваемые параметры, которые не назначены другим переменным. Оставшиеся параметры являются массивом.

В данном примере, переменной `a` назначено значение `true`. Получается, все остальные значения (`false` и `false`) будут записаны в `params`.

</p>
</details>

---

##### 7. Какой будет вывод?

```javascript
fn()

function fn() {
  console.log('Hello')
}
```

1. `'Hello'`
2. `undefined`
3. `null`
4. `ReferenceError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Функции, объявленные как **Function declaration**, можно вызывать до того места где они записаны в коде.

</p>
</details>

---

##### 8. Какой будет вывод?

```javascript
fn()

const fn = function() {
  console.log('World')
}
```

1. `'World'`
2. `undefined`
3. `null`
4. `ReferenceError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Функции, объявленные как **Function definition**, нельзя вызывать до того места, где они записаны в коде.

Это отличает объявление Function definition от Function declaration.

</p>
</details>





















