<div align="center">

# Тесты: String, кавычки, конкатенация, методы

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
const city = 'Москва'
const address = 'Ленинский проспект'
const house = '10А'
console.log(city + address + house)
```

1. `Москва Ленинский проспект 10А`
2. `МоскваЛенинский проспект10А`
3. `Москва, Ленинский проспект, 10А`
4. `Москва`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Конкатенация (сложение) строк происходит без добавления символов движком "от себя" — если между строками не было пробелов или запятых — то и в итоговой строке их не будет.

</p>
</details>
