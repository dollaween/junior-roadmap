<div align="center">

## Задачи
# Строки

[Главная](https://github.com/dollaween/junior-roadmap/)
|
[Карта](/roadmap/README.md)
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



