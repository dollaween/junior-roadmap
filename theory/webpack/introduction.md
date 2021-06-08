<div align="center">

# Введение в Webpack

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

**Webpack** — это инструмент, который помогает собирать проекты.

С помощью Webpack можно:
- Объединять несколько файлов в один.
- Преобразовывать файлы. Например, SASS в CSS или Typescript в Javascript.
- Перемещать файлы.

---

<div align="center">

### Установка

</div>

---

```bash
mkdir webpack-demo
npm init
npm i webpack webpack-cli
```

---

<div align="center">

### CLI команды

</div>

---

```bash
# Запускает процесс сборки
npx webpack --config webpack.config.js
```

---

<div align="center">

### Loaders

</div>

---

Из коробки, Webpack умеет работать только с Javascript и JSON файлами. Чтобы работать с другими типами данных, для каждого типа нужно установить свой лоадер.

`test` — выбирает файлы по регулярному выражению.  
`use` — применяет к выбранным файлам лоадер.

#### CSS

```bash
npm install --save-dev style-loader css-loader
```

**style-loader** — внедряет CSS в DOM.  
**css-loader** — интерпретирует `@import` и `url()`.

```
# webpack.config.js
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist'),
  },
  module: {
    rules: [
      {
        test: /\.css$/i,
        use: ['style-loader', 'css-loader'],
      },
    ],
  },
};
```


