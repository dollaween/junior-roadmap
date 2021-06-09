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
- Минифицировать файлы.
- Находить и удалять неиспользуемый код.

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
# Запускает процесс сборки с указанием конфигурационного файла
npx webpack --config webpack.config.js
```

---

<div align="center">

### Конфиг

</div>

---

`mode`:
- `development` — не минифицирует итоговый бандл.
- `production` — миницифирует итоговый бандл.

---

<div align="center">

### Loaders

</div>

---

Из коробки, Webpack умеет работать только с Javascript и JSON файлами. Чтобы работать с другими типами файлов, для каждого из них нужно установить свой лоадер.

Лоадер имеет два свойства в конфигурационном файле:
1. `test` — выбирает файлы по регулярному выражению.
2. `use` — применяет к выбранным файлам лоадер. Лоадеров может быть несколько. В таком случае, начиная с последнего, каждый из них будет что-то делать с файлом и отдавать результат следующему лоадеру. Первый лоадер в списке вернет итоговый результат (который ожидается в виде Javascript).

---

<div align="center">

### Загрузка CSS

</div>

---

```bash
npm install --save-dev style-loader css-loader
```

**style-loader** — внедряет CSS в DOM.

**css-loader** — обрабатывает `@import` и `url()`, .

| Свойство | Тип | По-умолчанию | Описание
| --- | --- | --- | ---
| `url` | `Boolean/Function` | `true` | Включает/выключает обработку `url / image-set`. Если передать функцию — то можно определять, как обрабатывать конкретные url.
| `import` | `Boolean` | `true` | Включает/выключает обработку `@import`
| 


| Свойство | Тип                | По-умолчанию | Описание                                                                                                                      |
| -------- | ------------------ | ------------ | -------- |
| `url`    | `Boolean/Function` | `true`       | Включает/выключает обработку `url / image-set`. Если передать функцию — можно определять, как обрабатывать конкретные url. |
| `import` | `Boolean/Function` | `true`       | Включает/выключает обработку `@import`. Если передать функцию — можно убирать обработку отдельных файлов лоадером |
| 


После того, как эти лоадеры будут запущены, будет создан тег `style` со стилями и помещен в тег `head`.

```js
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

---

<div align="center">

### Загрузка изображений

</div>

---

Для скачанных изображений и иконок нужен лоадер.

```js
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
      {
        test: /\.(png|svg|jpg|jpeg|gif)$/i,
        type: 'asset/resource',
      }
    ],
  },
};
```

Пример использования в CSS:
```css
.img {
  width: 200px;
  height: 150px;
  background-image: url('./terminator.jpeg');
  background-size: cover;
}
```

Пример использования в JS:
```js
import Icon from './icon.png';

function component() {
  const element = document.createElement('div');

  const myIcon = new Image();
  myIcon.src = Icon;

  element.appendChild(myIcon);

  return element;
}

document.body.appendChild(component());
```

