<div align="center">

# Псевдоклассы и псевдоэлементы

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

##### 1. Когда цвет кнопки будет становиться зеленым?

```html
<button>Example button</button>
```

```css
button:hover {
  color: green;
}
```

1. Всегда
2. При нажатии на кнопку
3. При наведении на кнопку
4. Никогда

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Псевдокласс `:hover` срабатывает, когда пользователь наводит на элемент мышью.

</p>
</details>

---

##### 2. Когда цвет фона элемента `p` будет становиться зеленым?

```html
<p>Example text</p>
```

```css
p:active {
  background: green;
}
```

1. При нажатии на элемент
2. При наведении на элемент
3. При перемещении к элементу кнопкой TAB
4. Никогда

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Псевдокласс `:active` срабатывает, когда пользователь активирует элемент.

</p>
</details>

---

##### 3. Когда цвет фона элемента `div` будет становиться зеленым?

```html
<div>Example text</div>
```

```css
div:focus {
  background: green;
}
```

1. При нажатии на элемент
2. При наведении на элемент
3. При перемещении к элементу кнопкой TAB
4. Никогда

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  Псевдокласс `:focus` срабатывает, когда пользователь устанавливает фокус на элементе. Но не все элементы имеют состояние "фокус" (например, `div`), его нужно добавить вручную. Для этого необходимо добавить нужному элементу атрибут `tabindex`.

</p>
</details>

---

##### 4. При каком условии элемент `div` будет иметь зеленый цвет фона?

```html
<div>
  <input type="text" autofocus>
</div>
```

```css
div:focus-within {
  background: green;
}
```

1. При установке фокуса на `input`
2. При установке фокуса на `div`
3. При потере фокуса
4. Никогда

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Псевдокласс `:focus-within` срабатывает, когда либо сам элемент имеет фокус, либо содержит элемент, который имеет фокус. Без атрибута `tabindex` на `div` установить фокус нельзя.

</p>
</details>

---

##### 5. Какой из элементов будет окрашен в зеленый цвет?

```html
<div>
  <span>First element</span>
  <div>Second element</div>
  <p>Third element</p>
</div>
```

```css
p:first-child {
  background: green;
}
```

1. `span`
2. `div`
3. `p`
4. Никакой

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  Псевдокласс `:first-child` — находит элемент, который является первым в своем родителе.

  Элемент `p` — не является первым в списке.

</p>
</details>

---

##### 6. Какой из элементов будет окрашен в зеленый цвет?

```html
<div>
  <span>First element</span>
  <div>Second element</div>
  <p>Third element</p>
</div>
```

```css
div :last-child {
  background: green;
}
```

1. `span`
2. `div`
3. `p`
4. Никакой

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Псевдокласс `:last-child` — находит элемент, который является последним в своем родителе.

  Запись вида `div :last-child` (с пробелом перед двоеточием) аналогична записи `div *:last-child` — то есть будет найдет любой последний элемент внутри элемента `div`.

</p>
</details>

---

##### 7. Какие элементы `li` будет окрашены в зеленый цвет?

```html
<ul>
  <li>Element 1</li>
  <li>Element 2</li>
  <li>Element 3</li>
  <li>Element 4</li>
</ul>
```

```css
li:nth-child(odd) {
  background: green;
}
```

1. `1, 3`
2. `2, 4`
3. Все
4. Никакой

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**
  
  Псевдокласс `:nth-child()` — находит элемент на указанной позиции.

  Кроме указания конкретного элемента, поддерживаются два ключевых слова:
  - even — все нечетные элементы.
  - odd — все четные элементы.

</p>
</details>


---

##### 8. Какой из элементов `li` будет окрашен в зеленый цвет?

```html
<ul>
  <li>Element 1</li>
  <li>Element 2</li>
  <li>Element 3</li>
  <li>Element 4</li>
</ul>
```

```css
li:nth-child(2n-1) {
  background: green;
}
```

1. `1, 3`
2. `2, 4`
3. Все
4. Никакой

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Псевдокласс `:nth-child(2n - 1)` — находит каждый второй элемент, начиная с первого. Такая запись аналогична записи `:nth-child(even)`.

</p>
</details>

---

##### 9. Какой из элементов будет окрашен в зеленый цвет?

```html
<div>
  <span>First element</span>
  <div>Second element</div>
  <p>Third element</p>
</div>
```

```css
p:first-of-type {
  background: green;
}
```

1. `span`
2. `div`
3. `p`
4. Никакой

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Псевдокласс `:first-of-type` находит первый элемент указанного типа (тега).

</p>
</details>

---

##### 10. Какие из элементов будут окрашены в зеленый цвет?

```html
<div>
  <span>First element</span>
  <div>Second element</div>
  <p>Third element</p>
  <p>Fourth element</p>
  <p>Fifth element</p>
</div>
```

```css
div p:nth-of-type(2n) {
  background: green;
}
```

1. `2`
2. `4`
3. `2, 4`
4. `3, 5`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Псевдокласс `:nth-of-type()` — действует по аналогии с `:nth-child()`, но находит только элементы указанного типа (тега).

  Запись `p:nth-of-type(2n)` означает: найти каждый второй элемент `p`.

</p>
</details>

---

##### 11. Какой элемент будет окрашен в зеленый цвет?

```html
<ul>
  <li>Element 1</li>
  <li>Element 2</li>
</ul>
```

```css
ul :only-child {
  background: green;
}
```

1. Первый
2. Второй
3. Оба
4. Никакой

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  Псевдокласс `:only-child` — находит элемент, являющийся единственным потомком родителя.  
  Запись вида `ul :only-child` аналогична записи `ul *:only-child`.

  В данном примере, у элемента `ul` два потомка, поэтому стили применены не будут.

</p>
</details>

---

##### 12. Какой из элементов будет окрашен в зеленый цвет?

```html
<div>
  <span>Example span 1</span>
  <span>Example span 2</span>
  <p>Example paragraph</p>
</div>
```

```css
p:only-of-type {
  background: green;
}
```

1. Первый
2. Второй
3. Третий
4. Никакой

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Псевдокласс `:only-of-type` — находит элемент, который является единственным потомком такого типа (тега).

  Третий элемент является единственным типом `p` в `div`, поэтому стили будут применены к нему.

</p>
</details>

---

##### 13. Будет ли элемент `div` полупрозрачным?

```html
<div></div>
```

```css
div::after {
  content: '0'
}

div:empty {
  opacity: 0.5;
}
```

1. Да
2. Нет
3. В зависимости от свойства `content` в псевдоэлементе `::after`
4. В зависимости от расположения элемента `::after`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Псевдокласс `:empty` — находит элементы, у которых нет потомков. Псевдоэлементы не считаются потомками, поэтому `:empty` будет применен.

</p>
</details>

---

##### 14. Какие элементы будут окрашены в зеленый цвет?

```html
<div>
  <span>First element</span>
  <div>Second element</div>
  <p>Third element</p>
</div>
```

```css
div *:not(p, span) {
  background: green;
}
```

1. `2`
2. `1, 3`
3. `3`
4. `1, 2`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Псевдокласс `:not()` — исключает из нахождения элементы, которые указаны внутри скобок.

  Селектор `*:not(p, span)` — выбирает все элементы, кроме типов `p` и `span`.

</p>
</details>

---

##### 15. К какому элементу будут применены стили?

```html
<div required></div>
<div></div>
```

```css
div:required {
  background: green;
}
```

1. Первому
2. Второму
3. Всем
4. Никакому

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  Псевдокласс `:required` — находит элементы `<input>`, у которых есть атрибут `required`. У элемента `div` атрибут `required` не задается.

</p>
</details>

---

##### 16. К какому элементу будут применены стили?

```html
<input type="text" required>
<input type="text">
```

```css
input:optional {
  background: green;
}
```

1. Первому
2. Второму
3. Всем
4. Никакому

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Псевдокласс `:optional` противоположен псевдоклассу `:required` — он находит элементы `input`, у которых не задан атрибут `required`.

</p>
</details>

---

##### 17. Когда псевдокласс `:indeterminate` будет применен?

```html
<input type="radio" name="group">
<input type="radio" name="group">
```

```css
input[type="radio"]:indeterminate {
  opacity: .3;
}
```

1. Всегда к элементу установленному по-умолчанию
2. Когда ни одна из радио-кнопок не выбрана
3. Когда одна из радио-кнопок выбрана
4. Никогда, псевдокласс применим только к чекбоксам

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Псевдокласс `:indeterminate` — находит элементы в неопределенном состоянии.

  В данном примере, псевдокласс будет применен когда все элементы `<input type="radio">` в одной группе не выбраны.

</p>
</details>

---

##### 18. К какому элементу будут применены стили?

```html
<input type="radio" name="group" checked>
<input type="radio" name="group">
```

```css
input[type="radio"]:checked {
  opacity: 0.3;
}
```

1. Первому
2. Второму
3. Всем
4. Никакому

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Псевдокласс `:checked` — находит элементы `<input type="radio">`, `<input type="checkbox">` или `<option>`, которые выбраны или включены. В данном примере, с помощью атрибута `checked` выбран первый элемент.

</p>
</details>

---

##### 19. К какому элементу будут применены стили?

```html
<input type="radio" name="group" checked>
<input type="radio" name="group">
```

```css
input[type="radio"]:default {
  opacity: 0.3;
}
```

1. Первому
2. Второму
3. Всем
4. Никакому

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Псевдокласс `:default` — находит элемент установленный по-умолчанию. С помощью атрибута `checked` по-умолчанию отмечен первый `input`.

</p>
</details>

---

##### 20. К какому элементу будут применены стили?

```html
<div disabled>First element</div>
<p disabled>Second element</p>
<input type="text" disabled>
```

```css
*:disabled {
  background: grey;
}
```

1. Первому
2. Второму
3. Третьему
4. Никакому

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Псевдокласс `:disabled` — находит элементы `input`, `select`, у которых установлен атрибут `disabled`.

</p>
</details>

---

##### 21. Когда псевдокласс `:target` будет применен?

```html
<h2 id="section">Example heading</h2>
```

```css
#section1:target {
  color: orange;
}
```

1. Когда пользователь нажмет на элемент `h2`
2. Когда страница будет прокручена до элемента `h2`
3. Когда в url будет фрагмент `#section`
4. Когда элемент `h2` будет видимым на экране

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**
  
  Псевдокласс `:target` — находит элементы, атрибут `id` которых равен фрагменту `#` в url.

  Чтобы стили были применены к элементу `h2` нужно, чтобы url был вида `example.com/index.html#section`.

</p>
</details>

---

##### 22. К какому элементу будут применены стили? 

```html
<div>
  <p>Example text</p>
</div>
```

```css
p:root {
  background: green;
}
```

1. `div`
2. `p`
3. `html`
4. Никакому

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  Псевдокласс `:root` — находит корневой элемент. Он всегда указывает на элемент `html`, но должен быть записан без каких-либо дополнительных селекторов.

  Правильная запись:

  ```css
  :root {
    background: green;
  }
  ```

</p>
</details>

---

##### 23. К какой части документа будут применены стили?

```html
<p>Example first text. Example second text.</p>
```

```css
p::first-letter {
  color: green;
}
```

1. К первой букве первой строки
2. К первой букве каждой строки
3. К первой строке
4. К первому элементу внутри строки

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**
  
  Псевдоэлемент `::first-letter` — применяет стили к первой букве первой строки блочного элемента.

</p>
</details>

---

##### 24. К какой части документа будут применены стили?

```html
<p>Example first text. Example second text.</p>
```

```css
p::selection {
  color: green;
}
```

1. Псевдоэлемент `::selection` действует только на `input`-элементы
2. К первой строке элемента `p`
3. К выделенной части элемента `p`
4. К тексту элемента `p` заданного по-умолчанию

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Псевдоэлемент `::selection` — применяет стили к части документа, которую выделил пользователь (например, мышью).

</p>
</details>







