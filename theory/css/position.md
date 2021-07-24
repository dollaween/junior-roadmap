<div align="center">

# Позиционирование

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

**Позиционирование** — это изменение расположения элементов в документе.

За позиционирование отвечает свойство `position`. Его значения могут быть следующими:
- `static`
- `relative`
- `absolute`
- `fixed`
- `sticky`

У всех элементов, кроме тех у которых значение `static`, можно изменять позиционирование с помощью свойств:
- `top`
- `bottom`
- `left`
- `right`
- `z-index`

Типы позиционирования:
- **Позиционируемый элемент** — это элемент, у которого значение `position` является `relative`, `absolute`, `fixed` или `sticky` (другими словами, это все, кроме `static`).
- **Относительно позиционируемый элемент** — это элемент, значение `position` которого является `relative`.
- **Абсолютно позиционируемый элемент** — это элемент, чьё значение `position` является `absolute` или `fixed`.
- **Элемент с липкой позицией** — это элемент, у которого значение `position` является `sticky`.

---

<div align="center">

### `static`

</div>

---

Значение `static` — располагает элемент в его нормальное положение в документе. Это значение по-умолчанию для всех элементов на странице.

При значении `static`, у элемента недоступны следующие свойства: `top`, `right`, `bottom`, `left` и `z-index`.

```css
/* Ничего не изменится, потому что это итак значение по-умолчанию */
.block {
  position: static;
}
```

---

<div align="center">

### `relative`

</div>

---

Значение `relative` — располагает элемент в его нормальное положение в документе.

В отличие от `static`, такой элемент можно сдвигать с помощью свойств `top`, `right`, `bottom`, `left` и `z-index`.

```css
/* Элемент будет сдвинут на 20px вниз и на 40px вправо относительно его нормальной позиции */
.block {
  position: relative;
  top: 20px;
  left: 40px;
}
```

---

<div align="center">

### `absolute`

</div>

---

Значение `absolute`:
1. Удаляет элемент из нормального потока (то есть все остальные блоки располагаются так, как будто бы `absolute`-элемента не существует).
2. Затем `absolute`-элемент позиционируется относительно ближайшего позиционируемого предка.

> Обратите внимание, что `absolute`-элемент не будет позиционироваться относительно `static`-элементов. То есть если вы хотите, чтобы ваш элемент был справа сверху контейнера, то у контейнера нужно обязательно добавить `position: relative`.

```html
<div class="container">
  <div class="box"></div>
</div>
```

```css
.container {
  width: 500px;
  height: 200px;
  background: orange;
  margin: 200px auto;
  position: relative;
}

.box {
  position: absolute;
  top: 0;
  right: 0;
}
```

---

<div align="center">

### `fixed`

</div>

---

Значение `fixed`:
1. Удаляет элемент из нормального потока.
2. Располагает элемент относительно экрана браузера.

```css
/* Расположит элемент по центру экрана */
.block {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

---

<div align="center">

### `sticky`

</div>

---

Значение `sticky`:
1. Располагает элемент в его нормальное положение в документе.
2. Далее позиционирует элемент в зависимости от прокрутки ближайшего прокручиваемого предка.

Пример, когда при прокрутке документа, элемент будет прибит к верху окна браузера:
```css
body {
  height: 4000px;  /* Добавляем прокрутку */
}

.block {
  position: sticky;
  top: 0;
  margin: 200px 0;  /* Для наглядности, что элемент изначально не с самого верха документа */
}
```

---

<div align="center">

### `z-index`

</div>

---

Свойство [`z-index`](https://developer.mozilla.org/ru/docs/Web/CSS/z-index) — определяет положение позиционируемого элемента по оси z.

В случае, если два и более блоков расположены в одном и том же месте, последний из них перекроет все остальные. С помощью `z-index` мы можем вручную управлять, какой элемент будет расположен над другим.

Значения:
- `auto` — уровень элемента такой же, как и у родительского.
- Число — чем выше число, тем выше элемент.

Пример, при котором `.block-1` будет расположен над `.block-2`, потому что его `z-index` выше:
```css
.block-1 {
  width: 100px;
  height: 100px;
  position: fixed;
  left: 0;
  top: 0;
  background: orange;
  z-index: 2;
}

.block-2 {
  width: 50px;
  height: 50px;
  position: fixed;
  left: 0;
  top: 0;
  background: red;
  z-index: 1;
}
```

---

Источники:
- [MDN: Позиционирование](https://developer.mozilla.org/ru/docs/Learn/CSS/CSS_layout/Positioning)
- [`position`](https://developer.mozilla.org/ru/docs/Web/CSS/position)
- [`z-index`](https://developer.mozilla.org/ru/docs/Web/CSS/z-index)
