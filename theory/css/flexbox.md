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

Свойства, которые могут быть заданы flex-контейнеру:
* `flex-wrap`
* `flex-direction`
* `justify-content`
* `align-items`
* `gap`

Свойства, которые можно задавать отдельным элементам внутри flex-контейнера:
* `align-self`
* `flex`
* `flex-basis`
* `flex-grow`
* `flex-shrink`

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
* `baseline` — выравнивает элементы по базовой линии.

---

<div align="center">

### `flex-direction`

</div>

---

`flex-direction` — определяет, как будут расположены элементы внутри flex-контейнера.

Значения:
* `row` — элементы расположены по горизонтали, слева направо.
* `row-reverse` — элементы расположены по горизонтали, справа налево.
* `column` — элементы расположены по вертикали, сверху вниз.
* `column-reverse` — элементы расположены по вертикали, снизу вверх.

---

<div align="center">

### `flex`

</div>

---

`flex` — сокращение трех свойств в таком порядке: `flex-grow`, `flex-shrink`, `flex-basis`.

```css
.item {
  flex: 1 1 100%;
}
```

---

<div align="center">

### `flex-basis`

</div>

---

`flex-basis` — устанавливает ширину flex-элемента.

---

<div align="center">

### `flex-grow`

</div>

---

`flex-grow` — определяет, как много свободного пространства займет элемент.

Если применить `flex-grow` к одному элементу, то при значении:
* `0` — элемент не будет использовать свободное пространство.
* `0.5` — элемент займет половину свободного пространства.
* `1` — элемент займет все свободное пространство.

Если нескольким (или всем) элементам установить одинаковый `flex-grow`, то при значении:
* `0` — элементы не будут использовать свободное пространство.
* `1` — элементы поделят все свободное пространство поровну.
* `0.1` — каждый элемент заберет себе по 10% свободного пространства. В случае, когда элементов больше десяти, пространство будет поделено поровну.

Если элементам задать разное значение `flex-grow` — каждый из них будет использовать пропорционально столько пространства, сколько указано.

---

<div align="center">

### `flex-shrink`

</div>

---

`flex-shrink` — определяет фактор сжатия элемента. Свойство начинает действовать когда элементы не помещаются по ширине контейнера.

* `0` — элементы никогда не будут сжаты по ширине.
* `1` — элементы будут сжаты так, чтобы уместились по ширине в контейнер.

---

<div align="center">

### `align-self`

</div>

---

`align-self` — выравнивает flex-элемент по вертикали. Перезаписывает свойство `align-items` контейнера.

Значения такие же, как и у `align-items`.

---

<div align="center">

### `gap`

</div>

---

`gap` — задает пространство между flex-элементами.

---

Источники:
* [Flexbox](https://developer.mozilla.org/ru/docs/Learn/CSS/CSS_layout/Flexbox)
* [`flex-wrap`](https://developer.mozilla.org/ru/docs/Web/CSS/flex-wrap)
* [`align-items`](https://developer.mozilla.org/ru/docs/Web/CSS/align-items)
* [`justify-content`](https://developer.mozilla.org/ru/docs/Web/CSS/justify-content)
* [`flex-direction`](https://developer.mozilla.org/ru/docs/Web/CSS/flex-direction)
* [`flex`](https://developer.mozilla.org/ru/docs/Web/CSS/flex)
* [`flex-basis`](https://developer.mozilla.org/ru/docs/Web/CSS/flex-basis)
* [`flex-grow`](https://developer.mozilla.org/ru/docs/Web/CSS/flex-grow)
* [`flex-shrink`](https://developer.mozilla.org/ru/docs/Web/CSS/flex-shrink)
* [`align-self`](https://developer.mozilla.org/ru/docs/Web/CSS/align-self)
