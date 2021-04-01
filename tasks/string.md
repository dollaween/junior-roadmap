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

##### 2. Вывод первого символа строки

Дана строка ``. Выведите в консоль первый символ этой строки.

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

