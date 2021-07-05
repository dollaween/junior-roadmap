<div align="center">

# Jest

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

##### 1. Будет ли пройден тест?

```js
it('should sum a + b', () => {
  const a = 10
  const b = 5

  expect(a + b).toBe(15)
})
```

1. Да
2. Нет

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

</p>
</details>

---

##### 2. Будет ли пройден тест?

```js
it('should sum a + b', () => {
  const a = { count: 10 }
  const b = { count: 10 }

  expect(a).toBe(b)
})
```

1. Да
2. Нет

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**
  
  Будет ошибка — "Received: serializes to the same string".

  Объекты нужно сравнивать через утверждение `.toEqual`.
  
  ```js
  it('should sum a + b', () => {
    const a = { count: 10 }
    const b = { count: 10 }

    expect(a).toEqual(b)
  })
  ```

</p>
</details>



