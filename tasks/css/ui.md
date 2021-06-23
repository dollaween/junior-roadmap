<div align="center">

# Задачи по созданию UI-компонентов

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

##### 1. Создайте и стилизуйте компонент Input

![image](https://user-images.githubusercontent.com/48933270/123074398-eb331400-d41f-11eb-9846-438b07a09996.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A1)

<details><summary><b>Решение</b></summary>
<p>

```html
<input class="input" type="text" placeholder="Enter your login..">
```

```css
.input {
  width: 240px;
  font-size: 14px;
  padding: 8px 10px;
  border-radius: 4px;
  border: 1px solid #bfbfbf;
  cursor: pointer;
  outline: none;
}

.input:hover,
.input:focus {
  border-color: #000;
}

.input::placeholder {
  color: #bfbfbf;
}
```

</p>
</details>
