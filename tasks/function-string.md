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
Также функция должна вывести длину строки в консоль.

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

returnEvenChars('Hello')      // 'Hlo'
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

---

##### 9. Первая и последняя буквы

Напишите функцию, которая принимает строку и возвращает новую строку, состояющую из первой буквы в верхнем регистре, троеточия и последней буквы в верхнем регистре.  
Также функция должна вывести результат в консоль.

```js
function firstAndLastChar() { /* ... */ }

firstAndLastChar('Hello')           // 'H...O'
firstAndLastChar('something more')  // 'S...E'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function firstAndLastChar(str) {
  const firstChar = str[0].toUpperCase()
  const lastChar = str[str.length - 1].toUpperCase()
  const result = firstChar + '...' + lastChar

  console.log(result)

  return result
}
```

</p>
</details>

---

##### 10. Замена нечетных символов

Напишите функцию, которая принимает строку, все нечетные символы заменяет точками и возвращает получившуюся строку.  
Также функция должна вывести результат в консоль.

```js
function replaceOddChars() { /* ... */ }

replaceOddChars('Hello')  // 'H.l.o'
replaceOddChars('Something more')  // 'S.m.t.i.g.m.r.'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function replaceOddChars(str) {
  let result = ''
  
  for (let i = 0; i < str.length; i++) {
    if (i % 2 === 0) {
      result += str[i]
    } else {
      result += '.'
    }
  }
  
  console.log(result)
  
  return result
}
```

</p>
</details>

---

##### 11. Массив строк

Напишите функцию, которая принимает строку, разбивает её на слова и возвращает получившийся массив строк. Если в функцию передана пустая строка — верните `null`. Обратите внимание: если в строке содержатся пробелы в начале или конце — они должны быть удалены.    
Также функция должна вывести результат в консоль.

```js
function toArray() { /* ... */ }

toArray('Hello')              // ['Hello']
toArray('Show me the money')  // ['Show', 'me', 'the', 'money']
toArray('  Something more ')  // ['Something', 'more']
toArray('')                   // null
```

<details><summary><b>Решение</b></summary>
<p>

```js
function toArray(str) {
  if (str.length === 0) {
    return null
  }

  const trimmedStr = str.trim()
  const result = trimmedStr.split(' ')
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 12. Каждое слово — в консоль

Напишите функцию, которая принимает строку и выводит в консоль каждое слово этой строки.  
Также функция должна вывести результат в консоль.

```js
function consoleWords() { /* ... */ }

consoleWords('Something more')
// 'Something'
// 'more'

consoleWords('Show me the money')
// 'Show'
// 'me'
// 'the'
// 'money'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function consoleWords(str) {
  const arr = str.split(' ')

  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i])
  }
}
```

</p>
</details>

---

##### 13. Первая и последняя буква каждого слова

Напишите функцию, которая принимает строку и выводит в консоль первую и последнюю букву каждого слова.
Также функция должна вывести результат в консоль.

```js
function consoleCharInWords() { /* ... */ }

consoleCharInWords('Something more')
// 'S', 'g'
// 'm', 'e'

consoleCharInWords('Show me the money')
// 'S', 'w'
// 'm', 'e'
// 't', 'e'
// 'm', 'y'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function consoleCharInWords(str) {
  const arr = str.split(' ')
  
  for (let i = 0; i < str.length; i++) {
    const firstChar = arr[i][0]
    const length = arr[i].length
    const lastChar = arr[i][length - 1]
    console.log(firstChar, lastChar)
  }
}
```

</p>
</details>


---

##### 14. Заглавные первые буквы слов

Напишите функцию, которая принимает строку и возвращает новую строку, у которой первая буква каждого слова — заглавная.  
Также функция должна вывести результат в консоль.

```js
function upperCharInWords() { /* ... */ }

upperCharInWords('something more')     // 'Something More'
upperCharInWords('show me the money')  // 'Show Me The Money'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function upperCharInWords(str) {
  const arr = str.split(' ')

  for (let i = 0; i < arr.length; i++) {
    arr[i] = arr[i][0].toUpperCase() + arr[i].slice(1)
  }

  const result = arr.join(' ')
  console.log(result)

  return result
}
```

</p>
</details>




























