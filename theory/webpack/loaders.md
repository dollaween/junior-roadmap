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
2. `use` — применяет к выбранным файлам лоадер. Лоадеров может быть несколько, в таком случае, начиная с последнего, каждый из них будет что-то делать с файлом и отдавать результат следующему лоадеру. Первый лоадер в списке вернет итоговый результат (который ожидается в виде Javascript).

---

<div align="center">

### Загрузка CSS

</div>

---

```bash
npm install --save-dev style-loader css-loader
```

[**css-loader**](https://webpack.js.org/loaders/css-loader/) — обрабатывает `@import`, `url()`, включает/выключает CSS Modules, генерирует source maps.  
[**style-loader**](https://webpack.js.org/loaders/style-loader/) — внедряет CSS в DOM (путем вставки одного или нескольких тегов `<style>`/`<link>` в тег `<head>`), позволяет загружать CSS частями и только по требованию (lazy load), позволяет работать с переопределением DLLPlugin'ов. По-умолчанию CSS вставляется вниз тега `<head>`, что можно изменить.

Оба лоадера поддерживают разные ES синтаксисы.

> [Не рекомендуется использовать вместе `style-loader` и `mini-css-extract-plugin`](https://webpack.js.org/loaders/style-loader/#recommend).

Пример:
```js
// webpack.config.js
module.exports = {
  module: {
    rules: [
      {
        test: /\.css$/i,
        use: ['style-loader', 'css-loader']
      },
    ],
  },
};
```

Пример загрузки по требованию:
```js
// webpack.config.js
module.exports = {
  module: {
    rules: [
      {
        test: /\.css$/i,
        use: [{
          loader: 'style-loader',
          options: {
            injectType: 'linkTag'
          }
        }, 'css-loader']
      }
    ]
  }
};
```

```js
// index.js
import styles from './style.css';

// Стили будут загружены в <head> через три секунды
setTimeout(function() {
  styles.use()
}, 3000);
```

---

<div align="center">

### Загрузка SASS

</div>

---

```bash
npm install --save-dev style-loader css-loader sass-loader sass node-sass
```

**[sass-loader](https://webpack.js.org/loaders/sass-loader/)** — загружает Sass/SCSS файлы и преобразует их в CSS.

Пример:

```js
module.exports = {
  module: {
    rules: [
      {
        test: /\.s[ac]ss$/i,
        use: ['style-loader', 'css-loader', 'sass-loader']
      }
    ]
  }
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
import Icon from './terminator.jpeg';

const image = new Image();
image.src = Icon;

document.body.appendChild(image);
```

---

Источники:
* [`css-loader`](https://webpack.js.org/loaders/css-loader/)

