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

[Entry Points](https://webpack.js.org/concepts/entry-points/) — это точки входа в проект. Можно указывать как одну точку, так и несколько.

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

Точкам входа можно давать названия. Эти названия будут использованы при создании итогового файла (output).

```js
module.exports = {
  entry: {
    app: './src/app.js',
    adminApp: './src/adminApp.js'
  }
};
```

Если точки входа будут сгенерированы плагинами, то в качестве значения `entry` можно указать пустой объект `{}`.

---

<div align="center">

### Output

</div>

---
