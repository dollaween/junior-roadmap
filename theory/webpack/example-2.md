<div align="center">

# Сборка проекта: React 18, SVG

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
- Работать с React 18
- Работать с SASS
- Работать с изображениями и шрифтами
- Работать с SVG
- Автоматически пересобирать сборку и обновлять страницу (Live Reload)
- Генерировать HTML-файл
- Очищать папку `dist` при каждой сборке

`package.json`
```json
{
  "name": "wp",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "dev": "webpack --env mode=development",
    "watch": "webpack serve --open"
  },
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "webpack": "^5.72.1",
    "webpack-cli": "^4.9.2"
  },
  "dependencies": {
    "@babel/core": "^7.17.10",
    "@babel/preset-env": "^7.17.10",
    "@babel/preset-react": "^7.16.7",
    "@svgr/webpack": "^6.2.1",
    "babel-loader": "^8.2.5",
    "css-loader": "^6.7.1",
    "html-webpack-plugin": "^5.5.0",
    "node-sass": "^7.0.1",
    "path": "^0.12.7",
    "react": "^18.1.0",
    "react-dom": "^18.1.0",
    "sass": "^1.51.0",
    "sass-loader": "^12.6.0",
    "style-loader": "^3.3.1",
    "webpack-dev-server": "^4.9.0"
  }
}
```

`webpack.config.js`
```js
const path = require('path')
const HtmlWebpackPlugin = require('html-webpack-plugin')

module.exports = {
  mode: 'development',
  entry: './src/index.js',
  output: {
    filename: 'bundle.js',
    path: path.join(__dirname, 'dist'),
    clean: true
  },
  plugins: [
    new HtmlWebpackPlugin({
      title: 'Output'
    })
  ],
  devServer: {
    static: {
      directory: path.join(__dirname, 'dist'),
    },
    compress: true,
    port: 3000,
  },
  module: {
    rules: [
      {
        test: /\.(js|jsx)$/,
        exclude: /node_modules/,
        use: ['babel-loader'],
      },
      {
        test: /\.s[ac]ss$/i,
        use: ['style-loader', 'css-loader', 'sass-loader']
      },
      {
        test: /\.css$/i,
        use: ['style-loader', 'css-loader']
      },
      {
        test: /\.svg$/,
        exclude: /raw\.svg$/,
        use: ['@svgr/webpack'],
      },
      {
        test: /\.(png|jpg|jpeg|gif)$/i,
        type: 'asset/resource',
      },
      {
        test: /\.(woff|woff2|eot|ttf|otf)$/i,
        type: 'asset/resource',
      }
    ]
  }
}
```

`.babelrc`
```js
{
  "presets": [
    "@babel/preset-env",
    ["@babel/preset-react", {"runtime": "automatic"}]
  ]
}
```

`src/index.js`
```js
import { createRoot } from 'react-dom/client';

const body = document.getElementsByTagName('body')[0]
const div = document.createElement('div')
div.id = 'root'
body.appendChild(div)

const root = createRoot(div);

root.render(<div>App</div>);
```
