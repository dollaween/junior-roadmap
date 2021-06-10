<div align="center">

# Кэширование

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

#### Зачем
Браузеры используют кэширование для уменьшения нагрузки на трафик и более быстрой загрузки сайтов. Это может стать причиной того, что мы сделали изменение в файле, а браузер взял старую версию из кэша, не скачав обновленный файл.

Цель работы с кэширование в Webpack — сделать так, чтобы не измененные файлы браузер брал из кэша, а измененные — загружал заново.

#### Как
Браузер работает с именем файла. Если такое название файла у него уже есть — он постарается взять файл из кэша.

Решение:  
Каждому файлу добавляем к имени уникальный хэш. Если в файле были изменения — обновляем хэш в имени.

---

<div align="center">

### Добавление хэша к имени

</div>

---

Добавить хэш к имени можно при помощи `[contenthash]` в файле бандла.

Для автоматической подстановки названия бандла с хэшом в HTML — используется HTMLWebpackPlugin.

```js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  mode: 'development',
  entry: {
    index: './src/index.js',
    print: './src/print.js'
  },
  output: {
    filename: '[name].[contenthash].js',
    path: path.resolve(__dirname, 'dist'),
    clean: true
  },
  plugins: [
    new HtmlWebpackPlugin()
  ]
};
```


---

<div align="center">

### Хэширование библиотек

</div>

---

Хорошей практикой считается хэшировать библиотеки, так как они будут меняться гораздо реже, чем наш код.

Таким образом можно захэшировать папку `node_modules`:
```js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  mode: 'development',
  entry: {
    index: './src/index.js',
    print: './src/print.js'
  },
  output: {
    filename: '[name].[contenthash].js',
    path: path.resolve(__dirname, 'dist'),
    clean: true
  },
  optimization: {
    runtimeChunk: true,
    splitChunks: {
      cacheGroups: {
        vendor: {
          test: /[\\/]node_modules[\\/]/,
          name: 'vendors',
          chunks: 'all',
        },
      },
    }
  },
  plugins: [
    new HtmlWebpackPlugin(),
  ]
};
```

---

Источники:
* [Caching](https://webpack.js.org/guides/caching/)
