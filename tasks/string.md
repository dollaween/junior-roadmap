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

Даны две строки `Москва` и 'Ленинский проспект', а также число `10`. Используя конкатенацию строк выведите в консоль фразу `Москва, Ленинский проспект: 10`.

```js
console.log(/* ... */)
// 'Москва, Ленинский проспект: 10'
```

<details><summary><b>Решение</b></summary>
<p>

```js
const city = 'Москва'
const street = 'Ленинский проспект'
const house = 10

console.log(city + ', ' + street + ': ' + house)
```

</p>
</details>
