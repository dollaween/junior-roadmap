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

### `animation`

</div>

---

`animation` — сокращенное свойство.

```css
/* duration | timing-function | delay | iteration-count | direction | fill-mode | play-state | name */
animation: 3s ease-in 1s 2 reverse both paused slidein;

/* duration | timing-function | delay | name */
animation: 3s linear 1s slidein;

/* duration | name */
animation: 3s slidein;
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

<div align="center">

### `animation-iteration-count`

</div>

---

Свойство `animation-iteration-count` — определяет сколько раз будет проигрываться анимация.

Значения:
* Число
* `infinite` — бесконечно.

```css
div {
  animation-iteration-count: 7;
}

div {
  animation-iteration-count: 5.4;
}

div {
  animation-iteration-count: infinite;
}
```

---

<div align="center">

### `animation-direction`

</div>

---

Свойство `animation-direction` — определяет, должна ли анимация воспроизводиться вперёд, назад или переменно вперёд и назад.

Значения:
* `normal` — анимация проигрывается вперед. Когда анимация заканчивается — она сбрасывается и снова проигрывается.
* `reverse` — анимация проигрывается наоборот.
* `alternate` — анимация меняет направление в каждом цикле. Начинает с проигрывания вперед, затем назад и так далее.
* `alternate-reverse` — анимация меняет направление в каждом цикле. Начинает с конца, затем вперед и так далее.

---

<div align="center">

### `animation-fill-mode`

</div>

---

Свойство `animation-fill-mode` — определяет, как нужно применять стили к объекту анимации до и после её выполнения.

Значения:
* `none` — стили анимации не будут применены к элементу до и после её выполнения.
* `forwards` — по окончанию анимации элемент сохранит стили последнего ключевого кадра.
* `backwards` — элемент сохранит стиль первого ключевого кадра на протяжении периода `animation-delay`.
* `both` — анимация будет вести себя так, как будто значения `forwards` и `backwards` заданы одновременно.

---

<div align="center">

### `animation-play-state`

</div>

---

Свойство `animation-play-state` — определяет состояние анимации. Этим состоянием удобно управлять через скрипты.

Значения:
* `running` — анимация проигрывается.
* `paused` — анимация приостановлена.

---

Источники:
* [Использование CSS-анимации](https://developer.mozilla.org/ru/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
* [How to Use steps() in CSS Animations](https://designmodo.com/steps-css-animations/)
