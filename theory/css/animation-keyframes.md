<div align="center">

# Анимация через ключевые кадры

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

Для анимации через ключевые кадры необходимо:
1. Задать ключевые кадры в `@keyframes`.
2. Задать правила анимирования с помощью свойства `animation`.

---

<div align="center">

### `@keyframes`

</div>

---

Правило `@keyframes` — определяет стили для ключевых кадров.

Ключевые кадры определяются в процентах от 0 до 100. Для значений 0 и 100 есть алиасы — `from` и `to` соответственно.

Нижеследующий набор правил будет изменять цвет фона от белого к черному:

```css
@keyframes changeBackground {
  from {
    background: white;
  }

  to {
    background: black;
  }
}
```

---

Источники:
* [Использование CSS-анимации](https://developer.mozilla.org/ru/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
