<div align="center">

# Теория

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

[Code Splitting](https://webpack.js.org/guides/code-splitting/) — разделение одого большого файла на множество более мелких, которые в последствии можно подгружать по запросу или параллельно. С помощью этого можно добиться существенного влияния на скорость загрузки.

Существует три подхода к разделению кода:
1. С помощью Entry Points
2. Предотвращение дубликации
3. Динамические импорты

---

<div align="center">

### Entry Points

</div>

---

 C Entry Points все просто — указываем разные точки входа, файлы каждой из которых будут собираться в свой собственный бандл.

**webpack.config.js**
```js
const path = require('path');

module.exports = {
  entry: {
    index: './src/index.js',
    another: './src/another-module.js',
  },
  output: {
    filename: 'main.js',
    filename: '[name].bundle.js',
     path: path.resolve(__dirname, 'dist'),
  },
};
```

Если внутри разных бандлов есть ссылки на одни и те же библиотеки, или функции — этот код будет продублирован. Чтобы это предотвратить, мы можем общие библиотеки и код вынести в отдельный файл, на который бандлы будут в последствии ссылаться.

`dependOn` — свойство, которое определяет зависимость бандла. Перед сборкой бандла сперва будут собраны зависимости.

**webpack.config.js**
```js
const path = require('path');

module.exports = {
  mode: 'development',
  entry: {
    index: {
      import: './src/index.js',
      dependOn: 'shared',
    },
    another: {
      import: './src/another-module.js',
      dependOn: 'shared',
    },
    shared: 'lodash',
  },
  output: {
    filename: '[name].bundle.js',
    path: path.resolve(__dirname, 'dist'),
  },
};
```


