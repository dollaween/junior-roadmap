<div align="center">

# Watch и LiveReload

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

Для автоматической компиляции кода есть следующие инструменты:
1. Webpack Watch Mode
2. `webpack-dev-server`
3. `webpack-dev-middleware`

---

<div align="center">

### Webpack Watch Mode

</div>

---

[Watch Mode](https://webpack.js.org/guides/development/#using-watch-mode) — позволяет отслеживать зависимые файлы и запускать процесс сборки при их изменении.

Для этого запустите команду `webpack` с флагом `--watch`. Эту команду можно добавить в `package.json`:

```json
{
  "name": "webpack-demo",
  "version": "1.0.0",
  "scripts": {
    "build": "webpack",
    "watch": "webpack --watch"
  },
}
```

Единственный минус — эта команда не обновляет страницу в браузере автоматически.

---

<div align="center">

### `webpack-dev-server`

</div>

---

```bash
npm install --save-dev webpack-dev-server
```

[`webpack-dev-server`](https://webpack.js.org/guides/development/#using-webpack-dev-server) — представляет элементарный веб-сервер с возможностью перезагружать страницу в реальном времени.

**webpack.config.js**
```js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  mode: 'development',
  entry: ['./src/index.js', './src/print.js'],
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist'),
    clean: true
  },
  devServer: {
    contentBase: './dist'
  }
};
```

**package.json**
```json
{
  "name": "webpack-demo",
  "version": "1.0.0",
  "scripts": {
    "start": "webpack serve --open"
  },
}
```

---

<div align="center">

### `webpack-dev-middleware`

</div>

---

[`webpack-dev-middleware`](https://webpack.js.org/guides/development/#using-webpack-dev-server) — это обертка, которая отправляет файлы, обработанный Webpack'ом, на сервер.










