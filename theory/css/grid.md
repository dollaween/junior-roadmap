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
- `grid-gap`
- `grid-auto-rows`

Свойства, которые можно задавать отдельным элементам внутри grid-контейнера:
- `grid-column`
- `grid-row`

---

<div align="center">

### `grid-template-columns`

</div>

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






---

Источники:
- [`grid-template-columns`](https://developer.mozilla.org/ru/docs/Web/CSS/grid-template-columns)
- [`<flex> (fr)`](https://developer.mozilla.org/ru/docs/Web/CSS/flex_value)







