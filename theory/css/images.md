<div align="center">

# Работа с изображениями

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

### Работа с тегом `img`

</div>

---

Для стилизации тега `img` можно использовать следующие свойства: width, height, padding, margin, border, border-radius, object-position, object-fit.

---

`object-fit` — определяет, как изображение должно заполнять контейнер относительно его ширины и высоты.

Значения:
* `fill` — устанавливает ширину и высоту изображения равную ширине и высоте контейнера.
* `contain` — пропорционально подстраивает размеры изображения таким образом, чтобы оно полностью поместилось в контейнер.
* `cover` — пропорционально подстраивает размеры изображения таким образом, чтобы оно полностью покрыло весь контейнер.
* `none` — не изменяет размеры изображения.
* `scale-down` — сравнивает разницу между `none` и `contain`, и использует наименьший из вариантов.

---

`object-position` — выравнивает изображение внутри контейнера.

---

<div align="center">

### Работа с `background`

</div>

---

`background` — сокращенное свойство, которое устанавливает сразу все свойства стиля фона: цвет, изображение, источник, размер и метод повтора.

---

`background-color` — устанавливает цвет фона.

---

`background-image` — задает изображение для фона.

```css
.block {
  width: 200px;
  height: 200px;
  background-image: url('https://picsum.photos/200')
}
```

---

Источники:
* [Тег img](https://developer.mozilla.org/ru/docs/Web/HTML/Element/img)
* [`object-fit`](https://developer.mozilla.org/ru/docs/Web/CSS/object-fit)
* [`object-position`](https://developer.mozilla.org/ru/docs/Web/CSS/object-position)
