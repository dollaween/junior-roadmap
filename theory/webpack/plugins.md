<div align="center">

# Плагины

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

<div align="center">

### HtmlWebpackPlugin

</div>

---

```bash
npm install --save-dev html-webpack-plugin
```

[HtmlWebpackPlugin](https://github.com/jantimon/html-webpack-plugin) — автоматически генерирует `index.html` файл и вставляет в него бандлы из `output`.

```js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  entry: {
    index: './src/index.js',
    print: './src/print.js'
  },
  output: {
    filename: '[name].bundle.js',
    path: path.resolve(__dirname, 'dist')
  },
  plugins: [
    new HtmlWebpackPlugin({
      title: 'Output Management'
    }),
  ]
};
```
