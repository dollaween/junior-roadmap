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
  animation-duration: 5s, 800ms;
}
```

Если количество анимаций задано больше, чем значений `animation-duration`, то значения берутся циклически от начала до конца:

```css
div {
  animation-name: name1, name2, name3, name4, name5;
  animation-duration: 5s, 800ms;
}

/* Запись выше эквивалента этой: */
div {
  animation-name: name1, name2, name3, name4, name5;
  animation-duration: 5s, 800ms, 5s, 800ms, 5s, 800ms;
}
```

---

<div align="center">

### `animation-delay`

</div>

---

Свойство `animation-delay` — определяет время задержки перед началом анимации.

При указании отрицательного значения, воспроизведение анимации начнётся не с первого ключевого кадра, а так, будто часть анимации уже была показана.

---

<div align="center">

### `animation-timing-function`

</div>

---

Свойство `animation-timing-function` — определяет как происходит анимация в течение длительности.

Значения:
* `linear` — линейная анимация.
* `ease` — плавная анимация.
* `ease-in` — плавная в начале.
* `ease-out` — плавная в конце.
* `ease-in-out` — плавная в начале и конце.
* `step-start` — анимация по шагам.
* `step-end` — анимация по шагам.
* `steps(framesCount, end)` — разбивает анимацию между ключевыми кадрами на дополнительное количество кадров.

---

Источники:
* [Использование CSS-анимации](https://developer.mozilla.org/ru/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
* [How to Use steps() in CSS Animations](https://designmodo.com/steps-css-animations/)
