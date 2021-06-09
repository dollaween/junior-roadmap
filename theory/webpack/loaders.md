<div align="center">

# Загрузчики (Loaders)

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

[**style-loader**](https://webpack.js.org/loaders/style-loader/) — внедряет CSS в DOM.  
[**css-loader**](https://webpack.js.org/loaders/css-loader/) — обрабатывает `@import`, `url()`, включает/выключает CSS Modules, генерирует source maps.

После того, как эти лоадеры будут запущены, будет создан тег `style` со стилями и помещен в тег `head`.

```js
// webpack.config.js
module.exports = {
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
// webpack.config.js
module.exports = {
  module: {
    rules: [
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

---

Источники:
* [`css-loader`](https://webpack.js.org/loaders/css-loader/)

