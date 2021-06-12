<div align="center">

# Список тестов

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

##### 1. Какое значение свойства `color` будет у элемента `p`?

```html
<div>
  <p>Example text</p>
</div>
```

```css
div {
  color: green;
}
```

1. `black`
2. `green`
3. `inherit`
4. `unset`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3, 2**

Так как свойство `color` у элемента `p` не задано, то оно будет установлено в значение `inherit` (потому что `color` наследуется). После наследования, свойство приобритет значение `green`.

</p>
</details>

---
