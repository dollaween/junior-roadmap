<div align="center">

# Grid

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

**Grid** — это инструмент для создания сетки, с помощью которого можно располагать элементы на странице.

`display: grid` — задает grid-контейнер.

- Прямые дочерние элементы grid-контейнера больше не ведут себя как потоковые, а подчиняются новым правилам.

Свойства, которые могут быть заданы grid-контейнеру:
- `grid-template-columns`
- `grid-template-rows`
- `grid-template-areas`
- `grid-gap`
- `grid-auto-rows`

Свойства, которые можно задавать отдельным элементам внутри grid-контейнера:
- `grid-column`
- `grid-row`

---

<div align="center">

### `grid-template-columns`

</div>

---

`grid-template-columns` — задает количество столбцов и определяет их ширину.

Количество значений определяет количество столбцов:
- `grid-template-columns: 100%` — 1 столбец на всю ширину сетки.
- `grid-template-columns: 50% 50%` — 2 столбца по 50% ширины сетки.
- и так далее.

Возможные значения ширины столбца:
- В пикселях, процентах и других единицах измерения.
- `fr` — доля оставшегося пространства в сетке.
- `max-content` — ширина всего столбца будет стремиться к ширине ячейки с максимальным контентом.
- `min-content` — ширина всего столбца будет стремиться к ширине ячейки с минимальным контентом.
- `minmax(min, max)` — диапазон от `min` до `max`.
- `repeat(count, value)` — повторяет `value` столько раз, сколько указано в `count`. Используется для более компактной записи.
- `auto`.

Примеры:
- `grid-template-columns: 1fr 1fr 1fr` — три равных столбца.
- `grid-template-columns: repeate(12, 1fr)` — двенадцать равных столбцов.
- `grid-template-columns: 1fr 3fr 1fr` — второй столбец в три раза шире остальных.
- `grid-template-columns: 200px 1fr` — первый столбец `200px`, второй использует всю оставшуюся ширину.
- `grid-template-columns: repeat(auto-fill, 300px)` — создаст столько столбцов по `300px`, сколько влезет по ширине.


---

<div align="center">

### `grid-template-rows`

</div>

---

`grid-template-rows` — задает высоту рядов и их названия.

Количество значений определяет к каким столбцам будут применены значения:
- `grid-template-rows: 100px` — только первый ряд будет высотой `100px`, а все остальные `auto`.
- `grid-template-rows: 100px 100px` — два ряда будут высотой по `100px`, а все остальные `auto`.
- и так далее.

Возможные значения аналогичны `grid-template-columns`.

---

<div align="center">

### `grid-template-areas`

</div>

---

`grid-template-areas` — определяет названия grid-области.

Пример:
```css
.grid {
  grid-template-areas: "a a a"
                       "b c c"
                       "b c c";
}
```

---

<div align="center">

### `grid-template-areas`

</div>

---

---

<div align="center">

### Фишки

</div>

---

Ряды в Grid можно оборачивать дополнительным элементом. Но чтобы сетка не сломалась, дополнительным элементам нужно задать `display: contents`.

Пример верстки таблицы на Grid:

```html
<div class="table">
  <div class="row">
    <div class="cell">1</div>
    <div class="cell">Terminator</div>
    <div class="cell">26.10.1984</div>
  </div>
  <div class="row">
    <div class="cell">2</div>
    <div class="cell">Robocop</div>
    <div class="cell">17.07.1987</div>
  </div>
</div>
```

```css
.table {
  display: grid;
  grid-template-columns: max-content 1fr max-content;
  width: 400px;
}

.row {
  display: contents;
}

.row:nth-child(odd) > .cell {
  background: #ddd;
}

.row:hover > .cell {
  background: #ccc;
}

.cell {
  padding: 4px 8px;
  border: 1px solid #ddd;
}
```

---

Источники:
- [CSS Grid Layout](https://developer.mozilla.org/ru/docs/Web/CSS/CSS_Grid_Layout)
- [`grid-template-columns`](https://developer.mozilla.org/ru/docs/Web/CSS/grid-template-columns)
- [`grid-template-rows`](https://developer.mozilla.org/ru/docs/Web/CSS/grid-template-rows)
- [`grid-template-areas`](https://developer.mozilla.org/ru/docs/Web/CSS/grid-template-areas)
- [`grid-template`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template)
- [`<flex> (fr)`](https://developer.mozilla.org/ru/docs/Web/CSS/flex_value)







