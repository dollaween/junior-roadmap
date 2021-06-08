<div align="center">

# Анимация через ключевые кадры

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

Для анимации через ключевые кадры необходимо:
1. Задать ключевые кадры в `@keyframes`.
2. Задать правила анимирования с помощью свойства `animation`.

---

<div align="center">

### `@keyframes`

</div>

---

Правило `@keyframes` — определяет стили для ключевых кадров.

Ключевые кадры определяются в процентах от 0 до 100. Для значений 0 и 100 есть алиасы — `from` и `to` соответственно.

Нижеследующий набор правил будет увеличивать элемент в два раза:

```css
@keyframes changeScale {
  from {
    transform: scale(1);
  }

  to {
    transform: scale(2);
  }
}
```

Можно изменять несколько свойств одновременно. Ключевых кадров тоже может быть несколько.

```css
@keyframes changeColors {
  0% {
    background: white;
    border: 1px solid black;
  }

  30% {
    background: red;
    border: 1px solid green;
  }

  60% {
    background: blue;
    border: 1px solid red;
  }

  100% {
    background: black;
    border: 1px solid white;
  }
}
```

---

<div align="center">

### `animation-name`

</div>

---

Свойство `animation-name` — задает элементу указанные названия анимаций (которые мы использовали в @keyframes).

```css
div {
  animation-name: changeColors, changeScale;
}
```

---

<div align="center">

### `animation-duration`

</div>

---

Свойство `animation-duration` — определяет продолжительность анимации в секундах или миллисекундах.

```css
div {
  animation-duration: 1s;
}
```

Если задано несколько анимаций, то для каждой из них можно указать свою продолжительность:

```css
div {
  animation-name: changeColors, changeScale;
  animation-duration: 1s, 300ms;
}
```

Если количество анимаций задано больше, чем значений `animation-duration`, то значения берутся циклически от начала до конца:

```css
div {
  animation-name: name1, name2, name3, name4, name5;
  animation-duration: 1s, 300ms;
}

/* Запись выше эквивалента этой: */
div {
  animation-name: name1, name2, name3, name4, name5;
  animation-duration: 1s, 300ms, 1s, 300ms, 1s, 300ms;
}
```

---

Источники:
* [Использование CSS-анимации](https://developer.mozilla.org/ru/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
