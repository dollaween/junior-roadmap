<div align="center">

# Псевдоклассы

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

**Псевдокласс** — это ключевое слово, добавленное к селектору, которое определяет его особое состояние.

Псевдоклассы позволяют добавлять стили к элементам, основываясь на позиции курсора мыши (`:hover`), состоянии содержимого (`:checked`) или истории посещения (`:visited`).

---

<div align="center">

### `:hover`

</div>

---

Псевдокласс `:hover` срабатывает, когда пользователь наводит на элемент мышью.

В примере ниже, при наведении на элемент `button` курсора мыши, будет меняться его цвет фона:

```css
button {
  background: #333;
  color: #fff;
}

button:hover {
  background: #666;
}
```


---

<div align="center">

### `:active`

</div>

---

Псевдокласс `:active` срабатывает, когда пользователь активирует элемент.  
"Активирует" — означает время между нажатием и отпусканием кнопки мыши.

В примере ниже, при нажатии на элемент будет меняться цвет фона:

```css
button {
  background: #333;
  color: #fff;
}

button:active {
  background: #666;
}
```

---

<div align="center">

### `:focus`

</div>

---

Псевдокласс `:focus` срабатывает, когда пользователь устанавливает фокус на элементе.  
Фокус можно установить путем:
1. Нажатия на элемент.
2. Перемещения к элементу с помощью клавиши TAB на клавиатуре.

```css
input {
  background: #fff;
}

input:focus {
  background: #ccc;
}
```

По-умолчанию, при установке фокуса на элемент, у него будет присутствовать рамка (свойство `outline`). Чтобы убрать эту рамку нужно установить `outline: none`.

```css
input:focus {
  background: #ccc;
  outline: none;
}
```

Не все элементы имеют состояние "фокус" (например, `div`), но его можно добавить вручную. Для этого необходимо добавить нужному элементу атрибут `tabindex`.

```html
<div tabindex="0"></div>
```

```css
div {
  width: 100px;
  height: 50px;
  background: green;
}

div:focus {
  background: orange;
}
```

---

Источники:
- [`:hover`](https://developer.mozilla.org/ru/docs/Web/CSS/:hover)
- [`:active`](https://developer.mozilla.org/ru/docs/Web/CSS/:active)
- [`:focus`](https://developer.mozilla.org/ru/docs/Web/CSS/:focus)

