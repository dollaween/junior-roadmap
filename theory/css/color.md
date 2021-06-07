<div align="center">

# Цвет

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

Цвет можно задавать несколькими способами:
* По ключевому слову.
* Через функцию `rgb()` или `rgba()`.
* Через хекс.
* Через функцию `hsl()` или `hsla()`.

---

Цвет можно задач с помощью ключевого слова, обозначающего цвет.

Список доступных ключевых слов можно найти здесь:  
[W3C Color keywords](https://www.w3.org/wiki/CSS/Properties/color/keywords)

```css
p {
  color: white;
  background: black;
  border: 1px solid tomato;
}
```

---

Функция `rgb()` принимает три параметра, которые отвечают за красный, зеленый и синий цвет.

```css
p {
  color: rgb(255, 255, 255);        // белый
  background: rgb(0, 0, 0);         // черный
  border: 1px solid rgb(255, 0 0);  // красный
}
```

Функция `rgba()` содержит дополнительный четвертый параметр, который отвечает за альфа-канал (прозрачность).

```css
div {
  background: rgba(0, 0, 0, .5);  // полупрозрачный черный фон
}
```

---

Функция `hsl()` принимает три параметра, которые отвечают за оттенок, насыщенность и яркость.

```css
p {
  color: hsl(120%, 100%, 100%);         // белый
  background: hsl(120%, 100%, 0);       // черный
  border: 1px solid hsl(0, 100%, 50%);  // красный
}
```

Функция `hsla()` содержит дополнительный четвертый параметр, который отвечает за альфа-канал (прозрачность).

```css
div {
  background: hsl(120%, 100%, 0, .5);  // полупрозрачный черный фон
}
```



---

Источники:
* [W3C Color keywords](https://www.w3.org/wiki/CSS/Properties/color/keywords)
* [<color>](https://developer.mozilla.org/ru/docs/Web/CSS/color_value)
