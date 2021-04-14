<div align="center">

# Работа со строками

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

##### 1. Первый символ строки

Напишите функцию, которая принимает строку и возвращает первый символ строки.  
Также функция должна вывести первый символ строки в консоль.

```js
function firstChar() { /* ... */ }

firstChar('Hello')          // 'H'
firstChar('Somthing more')  // 'S'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function firstChar(str) {
  const result = str[0]
  console.log(result)
  return result
}
```

</p>
</details>


---

##### 2. Количество символов в строке

Напишите функцию, которая принимает строку и возвращает количество символов в строке.  
Также функция должна вывести первый символ строки в консоль.

```js
function getLength() { /* ... */ }

getLength('Hello')           // 5
getLength('Something more')  // 14
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getLength(str) {
  const result = str.length
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 3. Последний символ строки

Напишите функцию, которая принимает строку и возвращает последний символ строки.  
Также функция должна вывести результат в консоль.

```js
function lastChar() { /* ... */ }

lastChar('Hello')           // 'o'
lastChar('Something more')  // 'e'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function lastChar(str) {
  const length = str.length
  const result = str[length - 1]
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 4. Первая заглавная буква

Напишите функцию, которая принимает строку и возвращает ту же строку, но первый символ должен быть заглавным.  
Также функция должна вывести результат в консоль.

```js
function upperFirstChar() { /* ... */ }

upperFirstChar('hello')           // 'Hello'
upperFirstChar('something more')  // 'Something more'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function upperFirstChar(str) {
  const firstChar = str[0].toUpperCase()
  const restChars = str.slice(1)
  const result = firstChar + restChars
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 5. Последняя заглавная буква

Напишите функцию, которая принимает строку и возвращает ту же строку, но последний символ должен быть заглавным.  
Также функция должна вывести результат в консоль.

```js
function upperLastChar() { /* ... */ }

upperLastChar('hello')           // 'hellO'
upperLastChar('something more')  // 'something morE'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function upperLastChar(str) {
  const lastChar = str[str.length - 1].toUpperCase()
  const restChars = str.slice(0, str.length - 1)
  const result = restChars + lastChar
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 6. Все символы — в консоль

Напишите функцию, которая принимает строку и выводит каждый её символ в консоль

```js
function consoleChars() { /* ... */ }

consoleChars('Hello')
// 'H'
// 'e'
// 'l'
// 'l'
// 'o'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function consoleChars(str) {
  for (let i = 0; i < str.length; i++) {
    console.log(str[i])
  }
}
```

</p>
</details>

---

##### 7. Только четные символы — в консоль

Напишите функцию, которая принимает строку и выводит в консоль только те символы, которые находятся по четному индексу.

```js
function evenChars() { /* ... */ }

evenChars('Hello')
// 'H'
// 'l'
// 'o'

evenChars('Something')
// 'S'
// 'm'
// 't'
// 'i'
// 'g'
```

<details><summary><b>Решение 1</b></summary>
<p>

```js
function evenChars(str) {
  for (let i = 0; i < str.length; i++) {
    if (i % 2 === 0) {
      console.log(str[i])
    }
  }
}
```

</p>
</details>

<details><summary><b>Решение 2</b></summary>
<p>

```js
function evenChars(str) {
  for (let i = 0; i < str.length; i += 2) {
    console.log(str[i])
  }
}
```

</p>
</details>

---

##### 8. Возвращение только четных символов

Напишите функцию, которая принимает строку и вырезает все нечетные символы и возвращает получившуюся строку.  
Также функция должна вывести результат в консоль.

```js
function returnEvenChars() { /* ... */ }

returnEvenChars('Hello')  // 'Hlo'
returnEvenChars('Something')  // 'Smtig'
```

<details><summary><b>Решение 1</b></summary>
<p>

```js
function returnEvenChars(str) {
  let result = ''

  for (let i = 0; i < str.length; i++) {
    if (i % 2 === 0) {
      result += str[i]
    }
  }
  
  console.log(result)

  return result
}
```

</p>
</details>

<details><summary><b>Решение 2</b></summary>
<p>

```js
function returnEvenChars(str) {
  let result = ''

  for (let i = 0; i < str.length; i += 2) {
    result += str[i]
  }
  
  console.log(result)

  return result
}
```

</p>
</details>





















