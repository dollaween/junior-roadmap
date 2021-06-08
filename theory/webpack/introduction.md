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

Из коробки, Webpack умеет работать только с Javascript и JSON файлами. Чтобы работать с другими типами файлов, для каждого из них нужно установить свой лоадер.

Лоадер имеет два свойства в конфигурационном файле:
1. `test` — выбирает файлы по регулярному выражению.
2. `use` — применяет к выбранным файлам лоадер. Лоадеров может быть несколько. В таком случае, начиная с последнего, каждый из них будет что-то делать с файлом и отдавать результат следующему лоадеру. Первый лоадер в списке вернет итоговый результат (который ожидается в виде Javascript).

#### CSS

```bash
npm install --save-dev style-loader css-loader
```

**style-loader** — внедряет CSS в DOM.  
**css-loader** — интерпретирует `@import` и `url()`.

После того, как эти лоадеры будут запущены, будет создан тег `style` со стилями и помещен в тег `head`.

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

#### SASS

```bash

```


