<div align="center">

# Flexbox

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

**Flexbox** — это набор инструментов для создания сложных и гибких макетов.

`display: flex` — задает флексбокс.

* Прямые дочерние элементы флексбокса больше не ведут себя как потоковые, а подчиняются новым правилам.
* Прямым дочерним элементам можно задавать размеры и отступы.
* По-умолчанию все дочерние элементы будут находится на одной строке, сколько бы их ни было.

```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
</div>
```

```css
.container {
  display: flex;
}
```

---

<div align="center">

### `flex-wrap`

</div>

---

`flex-wrap` — задает правило вывода элементов — в одну строку или в несколько.

Значения:
* `nowrap` — все элементы расположены в одну линию. Если элементы не помещаются по ширине — они будут пропорционально уменьшены.
* `wrap` — элементы расположены в несколько линий.


---

<div align="center">

### `justify-content`

</div>

---

`justify-content` — определяет, как будет распределено пространство между элементами по горизонтали.

Значения:
* `flex-start` — выравнивает элементы по левому краю.
* `flex-end` — выравнивает элементы по правому краю.
* `center` — выравнивает элементы по центру.
* `space-between` — распределяет элементы равномерно, при этом первый элемент прижат к левому краю, а последний — к правому.
* `space-around` — распределяет элементы равномерно, пустые пространства перед первым и после последнего элемента равны половине расстояния между парами соседних элементов.
* `space-evenly` — распределяет элементы равномерно, пустые пространства перед первым и после последнего элемента равны расстояниям между парами соседних элементов.

---

<div align="center">

### `align-items`

</div>

---

`align-items` — выравнивает элементы по вертикали.

Значения:
* `flex-start` — выравнивает элементы по верху.
* `flex-end` — выравнивает элементы по низу.
* `center` — выравнивает элементы по центру.
* `stretch` — растягивает элементы по высоте.
* `baseline` — выравнивает элементы по строке.










---

Источники:
* [Flexbox](https://developer.mozilla.org/ru/docs/Learn/CSS/CSS_layout/Flexbox)
* [`flex-wrap`](https://developer.mozilla.org/ru/docs/Web/CSS/flex-wrap)
* [`align-items`](https://developer.mozilla.org/ru/docs/Web/CSS/align-items)
* [`justify-content`](https://developer.mozilla.org/ru/docs/Web/CSS/justify-content)

