<div align="center">

# Тесты: Приведение примитивных типов

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
const str = '40'
const num = 10

console.log(num + Number(str))
```

1. `50`
2. `4010`
3. `40Number(10)`
4. `NaN`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

При помещении параметра в объект `Number`, он попытается преобразовать параметр в число. Если преобразование в число невозможно, будет отдано значение `NaN`.

В данном случае, строка `40` будет преобразована в число `40`.

Примеры:
* `console.log(Number('12'))` -> `12`
* `console.log(Number('12 евро'))` -> `NaN`
* `console.log(Number(true))` -> `1`
* `console.log(Number(false))` -> `0`

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
const rub = '50 рублей'
const dol = 'долларов 30'

console.log(parseInt(rub) + parseInt(dol))
```

1. `30`
2. `50`
3. `80`
4. `NaN`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Функция `parseInt()` принимает строку и пытается преобразовать ее в число. Если преобразование не удается — будет возвращено значение `NaN`.

Если строка начинается с цифр, а затем идут другие символы — то будут возвращены цифры из начала строки (в преобразовании через объект `Number` будет возвращено значение `NaN`).

Примеры:
* `console.log(parseInt('10'))` -> `10`
* `console.log(parseInt('10 рублей'))` -> `10`
* `console.log(parseInt('10 или 5 рублей'))` -> `10`
* `console.log(parseInt('рублей 10'))` -> `NaN`

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
const hasAccess = true
const balance = '100'

console.log(+hasAccess + +balance)
```

1. `1`
2. `100`
3. `101`
4. `NaN`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Унарный оператор `+` превращает следуемый за ним тип данных в число. Работает так же, как прокидывание параметров в объект `Number`.

Примеры:
* `console.log(+'22')` -> `22`
* `console.log(+'20 рублей')` -> `NaN`
* `console.log(+true)` -> `1`
* `console.log(+false)` -> `0`

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
const float = '12.34'
console.log(typeof parseFloat(float))
```

1. `number`
2. `string`
3. `boolean`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Функция `parseFloat()` — принимает строку в качестве аргумента и возвращает число с плавающей точкой.

Оператор `typeof` возвращает строку, указывающую тип операнда.

Примеры `typeof`:
* `console.log(typeof 10)` -> `'number'`
* `console.log(typeof 'home')` -> `'string'`
* `console.log(typeof true)` -> `'boolean'`
* `console.log(typeof NaN)` -> `'number'`
* `console.log(typeof undefined)` -> `'undefined'`
* `console.log(typeof null)` -> `'object'`

Примеры `parseFloat()`:
* `console.log(parseFloat('10'))` -> `10`
* `console.log(parseFloat('10.501'))` -> `10.501`
* `console.log(parseFloat('str'))` -> `NaN`
* `console.log(parseFloat(true))` -> `NaN`

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
console.log(Boolean(1))
console.log(Boolean(0))
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Объект `Boolean` превращает передаваемый в него аргумент в `boolean` тип.

Значения `0`, `''`, `undefined`, `null`, `NaN`, `false` будут преобразованы в `false`. Все остальные значения будут преобразованы в `true`.

Примеры:
* `console.log(Boolean(10))` -> `true`
* `console.log(Boolean(0))` -> `false`
* `console.log(Boolean(-5))` -> `true`
* `console.log(Boolean('Hello'))` -> `true`
* `console.log(Boolean(''))` -> `false`
* `console.log(Boolean(NaN))` -> `false`
* `console.log(Boolean(undefined))` -> `false`
* `console.log(Boolean(null))` -> `false`
* `console.log(Boolean(false))` -> `false`

</p>
</details>



