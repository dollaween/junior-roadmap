<div align="center">

# Блочная модель

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

**Блочная модель (box model)** — модель, которая описывает из чего состоит элемент и какие свойства влияют на его размеры.

Каждый элемент состоит из прямоугольной области. В ней у каждого блока есть четыре области:
* Внешние отступы (margin)
* Рамка (border)
* Внутренние отступы (padding)
* Контент (content)

---

<div align="center">

### `box-sizing`

</div>

---

Свойство `box-sizing` — определяет, как будет вычисляться ширина и высота элемента.

Значение:
* `content-box` — к заданным размерам элемента будут добавлены внутренние отступы и рамка.
* `border-box` — внутренние отступы и рамка уже включены в заданные размеры элемента.

```css
/*
 * После всех вычислений:
 * Ширина: 200 + 10 * 2 + 15 * 2 = 250px
 * Высота: 100 + 10 * 2 + 15 * 2 = 150px
 */
.block-1 {
  box-sizing: content-box;
  width: 200px;
  height: 100px;
  border: 10px;
  padding: 15px;
}
```

```css
/*
 * После всех вычислений:
 * Ширина: 200
 * Высота: 100
 */
.block-2 {
  box-sizing: border-box;
  width: 200px;
  height: 100px;
  border: 10px;
  padding: 15px;
}
```

---

Источники:
* [Блоковая модель](https://developer.mozilla.org/ru/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
* [`box-sizing`](https://developer.mozilla.org/ru/docs/Web/CSS/box-sizing)

