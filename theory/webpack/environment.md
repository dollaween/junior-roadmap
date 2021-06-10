<div align="center">

# Переменные окружения (Environment Variables)

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

**Переменные окружения** — это объект с определенными данными, необходимыми для работы проекта.

Для работы Webpack, необходимо указать `mode`. Переменная окружения `env` — прекрасное место для хранения этой информации.

**package.json**
```json
{
  "name": "webpack-demo",
  "version": "1.0.0",
  "scripts": {
    "dev": "webpack --env mode=development",
    "prod": "webpack --env mode=production",
  },
}
```

Для использования переменной `env`, изменим экспорт с объекта на функцию:

**webpack.config.js**
```js
const path = require('path');

module.exports = function (env) {
  return {
    mode: env.mode,
    entry: './src/index.js',
    output: {
      filename: 'bundle.js',
      path: path.resolve(__dirname, 'dist')
    }
  };
};
```
