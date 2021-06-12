<div align="center">

# Единицы измерения

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

В CSS есть несколько видов единиц измерения: px, rem, em, %, vw, vh, vmin, vmax.

---

Пиксели `px` — это базовая единица измерения. Количество пикселей задается в настройках разрешения экрана.

* Любая другая единица измерения в итоге будет конвертирована в пиксели.
* Для расчетов можно использовать дробные значения пикселей, но при окончательном отображении они будут округлены.

```css
p {
  font-size: 16px;
  margin: 10px;
  line-height: 10px;
  border: 1px solid red;
}
```

---

`rem` — это относительная единица измерения, зависящая от значения `font-size` в теге `html`.

`1rem` равен значению `font-size` у элемента `html`.

```css
html {
  font-size: 16px;
}

p {
  font-size: 1rem;  /* 16px */
  margin-top: 2rem;  /* 32px */
}

h1 {
  font-size: 2.5rem;  /* 40px */
}
```

---

`em` — это относительная единица измерения:
* `font-size` у элемента зависит от значения `font-size` родителя. `1em` равен `font-size` в родительском теге.
* Все остальные значения свойств элемента зависят от своего `font-size`.

```html
<div>
  <p>Example <span>text</span></p>
</div>
```

```css
div {
  font-size: 16px;
}

p {
  font-size: 0.5em;  /* 8px */
  margin-top: 1em;  /* 8px */
}

span {
  font-size: 0.5em;  /* 4px */
  margin-top: 1em;  /* 4px */
}
```

---

* `vw` — 1% ширины окна.
* `vh` — 1% высоты окна.
* `vmin` — наименьшее из `vw`, `vh`.
* `vmax` — наибольшее из `vw`, `vh`.

---

Источники:
* [Единицы измерения: px, em, rem и другие](https://learn.javascript.ru/css-units)
