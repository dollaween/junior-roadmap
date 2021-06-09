<div align="center">

# Конфигурационный файл

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

Конфигурационный файл определяет настройки Webpack. По-умолчанию, Webpack будет искать файл с именем `webpack.config.js`.

---

<div align="center">

### Entry Points

</div>

---

Entry Points — это точки входа в проект. Можно указывать как одну точку, так и несколько.

```js
module.exports = {
  entry: './path/to/my/entry/file.js'
};
```

```js
module.exports = {
  entry: ['./src/file_1.js', './src/file_2.js']
};
```

Точкам входа можно давать названия. Это название будет использовано при создании output-файла.

```js
module.exports = {
  entry: {
    app: './src/app.js',
    adminApp: './src/adminApp.js'
  }
};
```

---

<div align="center">

### Output

</div>

---
