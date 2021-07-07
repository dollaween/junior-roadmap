<div align="center">

# Работа с текстом

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

<div align="center">

### `color`

</div>

---

Свойство `color` — задает цвет текста.  
Цвет может быть указан несколькими способами (подробнее в главе [«Цвет»](./color.md)).

```css
p {
  color: green;
}
```

---

<div align="center">

### `font`

</div>

---

Свойство `font` — это сокращение для свойств `font-style`, `font-variant`, `font-weight`, `font-stretch`, `font-size`, `line-height` и `font-family`.

---

<div align="center">

### `font-size`

</div>

---

Свойство `font-size` — определяет размер шрифта.  
Размер шрифта может быть задан с помощью нескольких единиц измерения (подробнее в главе [«Единицы измерения»](./units.md))

```css
p {
  font-size: 18px;
}
```

---

<div align="center">

### `font-weight`

</div>

---

Свойство `font-weight` — определяет насыщенность шрифта (то есть его жирность).

Доступные значения:
- Числа `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`, чем больше — тем жирнее начертание шрифта. Не у всех шрифтов есть все типы начертаний, у многих есть только `400` и `700`.
- Ключевые слова `regular` (аналогичен значению `400`) и `bold` (аналогичен значению `700`).

```css
p {
  font-weight: 700;
}

span {
  font-weight: bold;
}
```

---

<div align="center">

### `letter-spacing`

</div>

---

Свойство [`letter-spacing`](https://developer.mozilla.org/ru/docs/Web/CSS/letter-spacing) — определяет расстояние между буквами в тексте.  
Положительные значения увеличивают расстояние между буквами, отрицательные значения — уменьшают.

```css
p {
  letter-spacing: 4px;
}
```

---

Источники:
- [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
- [`font-size`](https://developer.mozilla.org/ru/docs/Web/CSS/font-size)
- [`font-weight`](https://developer.mozilla.org/ru/docs/Web/CSS/font-weight)
- [`letter-spacing`](https://developer.mozilla.org/ru/docs/Web/CSS/letter-spacing)
