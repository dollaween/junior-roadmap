<div align="center">

# `vertical-align`

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

Свойство `vertical-align` — определяет, как будут позиционироваться элементы, значение свойства `display` которых `inline`, `inline-block` или `table-cell`.

> Это свойство нельзя использовать для вертикального выравнивания блочных элементов.

#### Значения относительно родительского элемента
Данные значения позиционируют элемент по вертикали относительно родительского элемента:
- `baseline` — выравнивает базовую линию элемента с базовой линией родительского элемента.
- `sub` — выравнивает базовую линию элемента с базовой линией подстрочного индекса своего родителя.
- `super` — выравнивает базовую линию элемента с базовой линией надстрочного индекса своего родителя.
- `text-top` — выравнивает верхний край элемента с верхним краем шрифта родительского элемента.
- `text-bottom` — выравнивает нижний край элемента с нижним краем шрифта родительского элемента.
- `middle` — выравнивает середину элемента с базовой линией своего родителя плюс половина от его высоты.
- `<length>` — поднимает базовую линию элемента на указанную величину над базовой линией родительского элемента. Допустимы отрицательные значения.
- `<percentage>` — поднимает базовую линию элемента на указанную в процентах величину (вычисляется относительно значения свойства `line-height`) над базовой линией родительского элемента. Допустимы отрицательные значения.

#### Значения относительно строки
Следующие значения позиционируют элемент по вертикали относительно всей строки:
- `top` — выравнивает верхний край элемента и его потомков с верхним краем всей строки.
- `bottom` — выравнивает нижний край элемента и его потомков с нижним краем всей строки.

По-умолчанию, значение свойства установлено в `baseline`.

Ниже приведен скриншот, с указанием, на какую позицию будет ссылаться то или иное значение свойства `vertical-align`:

![Пример](https://i.stack.imgur.com/Ousrm.gif)

---

Источники:
- [`vertical-align`](https://developer.mozilla.org/ru/docs/Web/CSS/vertical-align)
- [font-size vs line-height vs actual height](https://stackoverflow.com/questions/41336177/font-size-vs-line-height-vs-actual-height)
