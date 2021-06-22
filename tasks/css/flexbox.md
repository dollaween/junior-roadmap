<div align="center">

# Задачи на Flexbox

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

> Во всех решениях перед стилями подключен файл [`reset.css`](https://meyerweb.com/eric/tools/css/reset/).  
> Вы можете использовать [`normalize.css`](https://necolas.github.io/normalize.css/) или не использовать сброс стилей вовсе. В таком случае решения могут немного отличаться.

---

##### 1. Расположите элементы так, как показано на скриншоте

Каждый элемент должен занимать равную долю ширины родительского контейнера. Если элемента 2 — то каждый занимает по 50%, если элементов 4 — то каждый занимает по 25%, и так далее.

![image](https://user-images.githubusercontent.com/48933270/122951770-34cf2080-d386-11eb-9b55-95dfa8c32510.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A17)

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

```css
.container {
  display: flex;
}

.item {
  height: 150px;
  background: #69c0ff;
  border: 10px solid #1890ff;
  flex-grow: 1;
}
```

</p>
</details>
