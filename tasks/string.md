<div align="center">

## Задачи
# Строки

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

##### 1. Конкатенация строк

Даны две строки `Москва` и `Ленинский проспект`, а также число `10`. Используя конкатенацию строк выведите в консоль фразу `Москва, Ленинский проспект: 10`.

*Решите задачу двумя способами*

```js
console.log(/* ... */)
// 'Москва, Ленинский проспект: 10'
```

<details><summary><b>Решение 1</b></summary>
<p>

```js
const city = 'Москва'
const street = 'Ленинский проспект'
const house = 10

console.log(city + ', ' + street + ': ' + house)
```

</p>
</details>


<details><summary><b>Решение 2</b></summary>
<p>

```js
const city = 'Москва'
const street = 'Ленинский проспект'
const house = 10

console.log(`${city}, ${street}: ${house}`)
```

</p>
</details>

---

##### 2. Первый символ строки

Дана строка `Guardians of the Galaxy`. Выведите в консоль первый символ этой строки.

```js
console.log(/* ... */)
// G
```

<details><summary><b>Подсказка</b></summary>
<p>

Для вывода символа из строки используйте метод `charAt()`, либо квадратные скобки `[]`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const title = 'Guardians of the Galaxy'
console.log(title[0])
console.log(title.charAt(0))
```

</p>
</details>

---

##### 3. Последний символ строки

Дана строка `Guardians of the Galaxy`. Выведите в консоль последний символ этой строки.

```js
console.log(/* ... */)
// y
```

<details><summary><b>Подсказка</b></summary>
<p>

Для вывода последнего символа строки используйте свойство `length` и метод `charAt()` (либо квадратные скобки `[]`).

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const str = 'Guardians of the Galaxy'
console.log(str[str.length - 1])
console.log(str.charAt(str.length - 1))
```

</p>
</details>

---

##### 4. Поиск подстроки

Выведите в консоль `true`, если в строке есть указанная подстрока.

```js
const domain = 'https://google.com'

let char = 'google.com'
console.log(/* ... */)
// true

char = 'yahoo.com'
console.log(/* ... */)
// false
```

<details><summary><b>Подсказка</b></summary>
<p>

Для проверки нахождения подстроки в строке, используйте метод `includes()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const domain = 'https://google.com'

let char = 'google.com'
console.log(domain.includes(char))

char = 'yahoo.com'
console.log(domain.includes(char))
```

</p>
</details>

---

##### 5. Начало строки

Выведите в консоль `true`, если строка начинается с указанной подстроки, или `false` — если нет.

```js
const domain = 'https://github.com'

const protocolHTTP = 'http:'
console.log(/* ... */)
// false

const protocolHTTPS = 'https:'
console.log(/* ... */)
// true
```

<details><summary><b>Подсказка</b></summary>
<p>

Для определения, с какой подстроки начинается строка, используйте метод `startsWith()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const domain = 'https://github.com'
console.log(domain.startsWith('http:'))
console.log(domain.startsWith('https:'))
```

</p>
</details>

---

##### 6. Конец строки

Выведите в консоль `true`, если строка заканчивается указанной подстрокой, или `false` — если нет.

```js
const email = 'example@mail.com'

const template1 = 'mail.com'
console.log(/* ... */)
// true

const template2 = 'yahoo.com'
console.log(/* ... */)
// false
```

<details><summary><b>Подсказка</b></summary>
<p>

Для определения, какой подстрокой заканчивается строка, используйте метод `endsWith()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const email = 'example@mail.com'
console.log(email.endsWith('mail.com'))
console.log(email.endsWith('yahoo.com'))
```

</p>
</details>

---

##### 7. Верхний и нижний регистры

Приведите строку `email` к нижнему регистру, а строку `promocode` — к верхнему.

```js
const email = 'AwEsOme@mail.COM'
const promocode = 'fest'

console.log(/* ... */)
// awesome@mail.com

console.log(/* ... */)
// FEST
```

<details><summary><b>Подсказка</b></summary>
<p>

Для приведения строки к нижнему регистру используйте метод `toLowerCase()`.

Для приведения строки к верхнему регистру используйте метод `toUpperCase()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const email = 'AwEsOme@mail.COM'
const promocode = 'fest'

console.log(email.toLowerCase())
console.log(promocode.toUpperCase())
```

</p>
</details>

---

##### 8. Удаление пробелов с начала и конца строки

Удалите пробелы с начала и конца строки и выведите результат в консоль.

```js
const password = ' 123456  '

console.log(/* ... */)
// '123456'
```

<details><summary><b>Подсказка</b></summary>
<p>

Для обрезания пробельных символов с начала и конца строки используйте метод `trim()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const password = ' 123456  '
console.log(password.trim())
```

</p>
</details>

---

##### 9. Замена слов в строке

Дана строка `Jax Briggs`. Замените слово `Jax` на `Jacqui` и выведите в консоль

```js
const name = 'Jax Briggs'

console.log(/* ... */)
// Jacqui Briggs
```

<details><summary><b>Подсказка</b></summary>
<p>

Для замены подстроки в строке используйте метод `replace()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const name = 'Jax Briggs'
console.log(name.replace('Jax', 'Jacqui'))
```

</p>
</details>

---

##### 10. Замена всех слов в строке

Замените все слова `John` на `Megan` в строке и выведите в консоль.

```js
const message = 'John won. John earned 100 points. Good job, John'

console.log(/* ... */)
// 'Megan won. Megan earned 100 points. Good job, Megan'
```

<details><summary><b>Подсказка</b></summary>
<p>

Для замены всех вхождений подстроки в строке используйте метод `replaceAll()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const message = 'John won. John earned 100 points. Good job, John'
console.log(message.replaceAll('John', 'Megan'))
```

</p>
</details>

---

##### 11. Возвращение подстроки

Вырежьте из строки слово `they` и выведите его в консоль.

*Решите задачу двумя разными методами строки*

```js
const phrase = 'Johnny, they are in the trees'

console.log(/* ... */)
// 'they'
```

<details><summary><b>Подсказка</b></summary>
<p>

Для возвращения подстроки из строки используйте методы `slice()`, `substring()`.

</p>
</details>

<details><summary><b>Решение 1</b></summary>
<p>

```js
const phrase = 'Johnny, they are in the trees'

console.log(phrase.slice(8, 12))
```

</p>
</details>

<details><summary><b>Решение 2</b></summary>
<p>

```js
const phrase = 'Johnny, they are in the trees'

console.log(phrase.substring(8, 12))
```

</p>
</details>

---

##### 12. Кавычки в кавычках

Дана строка `'I'm "Frontend" developer!'`. В ней содержится ошибка. Исправьте ее и выведите в консоль.

```js
const greet = 'I'm "Frontend developer!"'

console.log(greet)
```

<details><summary><b>Решение</b></summary>
<p>

Если строка обернута одинарными кавычками, то одинарные кавычки в самой строке нужно экранировать специальным символом `\`.

```js
const greet = 'I\'m "Frontend developer!"'
console.log(greet)
```

</p>
</details>

---

##### 13. Разбиение строки на массив

Разбейте строку на массив строк, состоящих из слов исходной строки и выведите результат в консоль.

```js
const cartoon = 'Tom and Jerry'

console.log(/* ... */)
// ['Tom', 'and', 'Jerry']
```

<details><summary><b>Подсказка</b></summary>
<p>

Для разбиения строки на массив используйте метод `split()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const cartoon = 'Tom and Jerry'
console.log(cartoon.split(' '))
```

</p>
</details>

---

##### 14. Заглавная первая буква

Переведите первую букву в верхний регистр и выведите слово в консоль.

```js
const greet = 'hello'

console.log(/* ... */)
// Hello
```

<details><summary><b>Подсказка</b></summary>
<p>

Для перевода букв в верхний регистр, используйте метод `toUpperCase()`.

Для разбиения строки на подстроки, используйте метод `slice()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const greet = 'hello'

console.log(greet[0].toUpperCase() + greet.slice(1))
```

</p>
</details>


---

##### 15. Заглавная последняя буква

Переведите последнюю букву в верхний регистр и выведите слово в консоль.

```js
const greet = 'hello'

console.log(/* ... */)
// hellO
```

<details><summary><b>Подсказка</b></summary>
<p>

Для перевода букв в верхний регистр, используйте метод `toUpperCase()`.

Для разбиения строки на подстроки, используйте метод `slice()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const greet = 'hello'

const substring = greet.slice(0, greet.length - 1)
const lastChar = greet[greet.length - 1].toUpperCase()

console.log(substring + lastChar)
```

</p>
</details>









