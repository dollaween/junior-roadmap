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

### Mode

</div>

---

Значения свойства `mode`:
- `production` — миницифирует итоговый бандл.
- `development` — не минифицирует итоговый бандл.

**webpack.config.js**
```js
module.exports = {
  mode: 'development'
};
```

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

У точек входа есть дополнительные свойства, которые помогают установить порядок загрузки и другое — [EntryDescription object](https://webpack.js.org/concepts/entry-points/#entrydescription-object).

---

<div align="center">

### Output

</div>

---

Свойство [`output`](https://webpack.js.org/concepts/output/) — описывает, как и куда должен быть записан итоговый скомпилированный бандл.

> Если `entry points` может быть несколько, то `output` — только один.

Пример простой записи, при которой итоговый бандл будет записан в папку `/dist` с именем `bundle.js`:
```js
module.exports = {
  output: {
    filename: 'bundle.js',
    path: __dirname + '/dist'
  },
};
```

Пример конфигурации со множеством точек входа. Названия точек входа будет использовано в переменной `name`:
```js
module.exports = {
  entry: {
    app: './src/app.js',
    search: './src/search.js'
  },
  output: {
    filename: '[name].js',
    path: __dirname + '/dist'
  },
};
```

Свойство `clean` — очищает папку с бандлом перед каждым билдом.
```js
module.exports = {
  output: {
    filename: 'bundle.js',
    path: __dirname + '/dist',
    clean: true
  },
};
```

---

<div align="center">

### 

</div>

---

