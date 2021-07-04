<div align="center">

# Jest — `expect` и правила проверки

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

---

<div align="center">

### Правила

</div>

---

1. В качестве проверяемого значения нужно устанавливать конкретное значение или константу, чтобы избежать побочных эффектов.

Пример побочного эффекта:
```js
// Устанавливает страну у person2 такую же, как и у person1
function changeCountry(person1, person2) {
  person1.country = person2.country  // здесь допущена ошибка! должно было быть person2.country = person1.country
}

it('should move person2 to person1', function () {
  const person1 = { country: 'Spain' }
  const person2 = { country: 'Italy' }

  changeCountry(person1, person2)

  expect(person2.country).toBe(person1.country);
});
```

Мы допустили ошибку, но тест все равно пройден. Сейчас тест не проверяет, что именно в `person2` мы устанавливаем новое значение. Это надо исправить.

Правильное решение:
```js
// Устанавливает страну у person2 такую же, как и у person1
function changeCountry(person1, person2) {
  person1.country = person2.country  // все еще присутствует ошибка!
}

it('should move person2 to person1', function () {
  const PERSON1_COUNTRY = 'Spain'

  const person1 = { country: PERSON1_COUNTRY }
  const person2 = { country: 'Italy' }

  changeCountry(person1, person2)

  expect(person2.country).toBe(PERSON1_COUNTRY);
});
```

Теперь наш тест упадет и действительно отобразит ошибку.





