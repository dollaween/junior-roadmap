<div align="center">

# Пример сборки проекта

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

Данный билд умеет:
- Работать с SASS.
- Работать с изображениями и шрифтами.
- Автоматически пересобирать сборку и обновлять страницу (Live Reload).
- Генерировать HTML-файл.
- Генерировать хэш для имен файлов.
- Очищать папку `dist` при каждой сборке.

**package.json**
```json
{
  "name": "webpack-demo",
  "version": "1.0.0",
  "scripts": {
    "start": "webpack serve --open --env mode=development",
    "dev": "webpack --env mode=development",
    "prod": "webpack --env mode=production",
    "watch": "webpack --watch --env mode=development"
  },
  "devDependencies": {
    "css-loader": "^5.2.6",
    "html-webpack-plugin": "^5.3.1",
    "node-sass": "^6.0.0",
    "sass-loader": "^12.0.0",
    "style-loader": "^2.0.0",
    "webpack": "^5.38.1",
    "webpack-cli": "^4.7.2",
    "webpack-dev-server": "^3.11.2"
  }
}

```

**webpack.config.js**
```js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = function (env) {
  return {
    mode: env.mode,
    entry: './src/index.js',
    output: {
      filename: 'bundle.[contenthash].js',
      path: path.resolve(__dirname, 'dist'),
      clean: true
    },
    devServer: {
      contentBase: './dist'
    },
    module: {
      rules: [
        {
          test: /\.css$/i,
          use: ['style-loader', 'css-loader']
        },
        {
          test: /\.s[ac]ss$/i,
          use: ['style-loader', 'css-loader', 'sass-loader']
        },
        {
          test: /\.(png|svg|jpg|jpeg|gif)$/i,
          type: 'asset/resource',
        },
        {
          test: /\.(woff|woff2|eot|ttf|otf)$/i,
          type: 'asset/resource',
        }
      ]
    },
    plugins: [
      new HtmlWebpackPlugin(),
    ]
  };
};
```
