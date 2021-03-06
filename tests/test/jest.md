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

##### 1. Валиден ли следующий тест?

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

##### 2. Валиден ли следующий тест?

```js
it('should check equal between two objects', () => {
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

---

##### 3. Валиден ли следующий тест?

```js
it.each([
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
])('%i + %i should be %i', (a, b, expected) => {
  expect(a + b).toBe(expected)
})
```

1. Да
2. Нет

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**
  
  `it.each` — запускает тест несколько раз с указанным набором входных параметров.
  
  В данном случае, тест будет запущен три раза с параметрами:
  - `a = 1, b = 2, expected = 3`
  - `a = 4, b = 5, expected = 6`
  - `a = 7, b = 8, expected = 9`
  
  На второй и третий запуск тест пройден не будет.

</p>
</details>


---

##### 4. Валиден ли следующий тест?

```js
test.each`
  a    | b    | expected
  ${1} | ${1} | ${2}
  ${1} | ${2} | ${3}
  ${2} | ${1} | ${3}
`('returns $expected when $a is added $b', ({a, b, expected}) => {
  expect(a + b).toBe(expected)
})
```

1. Да
2. Нет

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Да, такая запись полностью валидна.

</p>
</details>

---

##### 5. Валиден ли следующий тест?

```js
// Устанавливает страну у person2 такую же, как и у person1
function changeCountry(person1, person2) {
  person2.country = person1.country
}

it('should move person2 to person1', function () {
  const person1 = { country: 'Spain' }
  const person2 = { country: 'Italy' }

  changeCountry(person1, person2)

  expect(person2.country).toBe(person1.country)
})
```

1. Да
2. Нет

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**
  
  Нет, тест не валиден, потому что при изменении `changeCountry` на `person1.country = person2.country` — тест не упадет, а должен.
  
  В утверждениях `.toBe` нужно использовать константы, чтобы избежать подобных побочных эффектов.
  
  ```js
  // Устанавливает страну у person2 такую же, как и у person1
  function changeCountry(person1, person2) {
    person2.country = person1.country
  }

  it('should move person2 to person1', function () {
    const PERSON1_COUNTRY = 'Spain'

    const person1 = { country: PERSON1_COUNTRY }
    const person2 = { country: 'Italy' }

    changeCountry(person1, person2)

    expect(person2.country).toBe(PERSON1_COUNTRY)
  })
  ```

</p>
</details>



