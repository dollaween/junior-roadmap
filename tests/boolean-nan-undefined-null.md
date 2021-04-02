<div align="center">

# Тесты: Boolean, NaN, undefined, null

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
const a = 5
const b = 2
const c = 4

console.log(a > b + c)
```

1. `true`
2. `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Оператор сложения `+` имеет более высокий приоритет, чем оператор больше `>`, поэтому в первую очередь будет выполнено сложение переменных `b` и `c`.

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
const str = '100'
const num = 100

console.log(str === num)
console.log(str == num)
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Оператор строгого равенства `===` проверяет, равны ли два его операнда с учетом их типов. `str` имеет тип 'строка', `num` имеет тип 'число'. Так как типы разные — будет возвращен `false`.

Оператор равенства `==` проверяет, равны ли два его операнда. В отличие от оператора строгого равенства, он попытается преобразовать и сравнить операнды разных типов. В данном случае, строка `str` будет преобразована в число и сравнена с переменной `num`, как числа.

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
const isLoginCorrect = true
const isPasswordCorrect = false
const canLogin = isLoginCorrect && isPasswordCorrect

console.log(canLogin)
```

1. `true`
2. `false`
3. `undefined`
4. `null`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Оператор 'логическое И' `&&` возвращает `true`, если оба его операнда истинны.

Примеры:
* `console.log(true && true)` -> `true`
* `console.log(true && false)` -> `false`
* `console.log(false && true)` -> `false`
* `console.log(false && false)` -> `false`

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
const canRead = true
const canWrite = false

console.log(canRead || canWrite)
```

1. `true`
2. `false`
3. `undefined`
4. `null`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Оператор 'логическое ИЛИ' возвращает `true`, если один из его операндов истинен.

Примеры:
* `console.log(true && true)` -> `true`
* `console.log(true && false)` -> `true`
* `console.log(false && true)` -> `true`
* `console.log(false && false)` -> `false`

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
const hasAccess = true

console.log(!hasAccess)
console.log(!!hasAccess)
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Оператор 'логическое НЕ' переводит `true` в `false` и обратно. Если оператор указан два раза — сперва будет вызван первый, затем второй.

Примеры:
* `console.log(!true)` -> `false`
* `console.log(!false)` -> `true`
* `console.log(!!true)` -> `true`
* `console.log(!!false)` -> `false`

</p>
</details>


---

Источники:
* [Приоритет операторов](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)
