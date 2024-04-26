<h1 align="center">Welcome to @omegion1npm/libero-delectus-laboriosam 👋</h1>
<p align="center">
  <img src="https://img.shields.io/npm/v/@omegion1npm/libero-delectus-laboriosam.svg?orange=blue" />
  <a href="https://www.npmjs.com/package/@omegion1npm/libero-delectus-laboriosam">
    <img alt="downloads" src="https://img.shields.io/npm/dm/@omegion1npm/libero-delectus-laboriosam.svg?color=blue" target="_blank" />
  </a>
  <a href="https://github.com/syukronarie/@omegion1npm/libero-delectus-laboriosam/blob/main/LICENSE">
    <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-yellow.svg" target="_blank" />
  </a>
  <a href="https://codecov.io/gh/syukronarie/@omegion1npm/libero-delectus-laboriosam">
    <img src="https://codecov.io/gh/syukronarie/@omegion1npm/libero-delectus-laboriosam/branch/main/graph/badge.svg" />
  </a>
  <a href="https://snyk.io/test/npm/@omegion1npm/libero-delectus-laboriosam">
    <img alt="snyk.io" src="https://snyk.io/test/npm/@omegion1npm/libero-delectus-laboriosam/badge.svg" target="_blank" /> 
  </a>
</p>

## ✨ What is @omegion1npm/libero-delectus-laboriosam?

`@omegion1npm/libero-delectus-laboriosam` is library to convert json raw (`array`) into xlsx file

## ⚡️ Installation

using npm

```zsh
npm install @omegion1npm/libero-delectus-laboriosam
```

using yarn

```zsh
yarn add @omegion1npm/libero-delectus-laboriosam
```

using pnpm

```zsh
pnpm add @omegion1npm/libero-delectus-laboriosam
```

## 🚀 Usage

Use to save as file:

```js
const @omegion1npm/libero-delectus-laboriosam = require('@omegion1npm/libero-delectus-laboriosam');
const fs = require('fs');

const json = [
  {
    name: 'John',
    age: 27,
    job: 'Software Engineer',
  },
];

const buffer = @omegion1npm/libero-delectus-laboriosam(json);

fs.writeFileSync('example.xlsx', buffer, 'binary');
```

Or use as express middleware. It adds a convenience `xlsx` method to the response object to immediately output an excel as download.

```js
const express = require('express');
const @omegion1npm/libero-delectus-laboriosam = require('@omegion1npm/libero-delectus-laboriosam');
const app = express();
const PORT = 3000;

const data = [
  {
    name: 'John',
    age: 27,
    job: 'Software Engineer',
  },
  {
    name: 'John',
    age: 27,
    job: 'Software Engineer',
  },
];

app.use(@omegion1npm/libero-delectus-laboriosam.middleware);
app.get('/', function (req, res) {
  res.xlsx('example.xlsx', data);
});

app.listen(PORT, function (err) {
  if (err) console.log(err);
  console.log('Server listening on PORT', PORT);
});
```

## 🤝 Contributing

Anyone can contribute with [issues](https://github.com/syukronarie/@omegion1npm/libero-delectus-laboriosam/issues) and [PRs](https://github.com/syukronarie/@omegion1npm/libero-delectus-laboriosam/pulls). If you're submitting a pull request, always create a new branch to work your changes, and try squashing commits down if possible. Always test any new code and make sure `npm test` passes and `npm run test:cover` for code coverage is adequate before opening a PR.

## Author

👤 **Arie Syukron**

- Github: [@syukronarie](https://github.com/syukronarie)

## Show your support

Please ⭐️ this repository if this project helped you!

<a href="https://www.patreon.com/syukronarie">
  <img src="https://c5.patreon.com/external/logo/become_a_patron_button@2x.png" width="160">
</a>

## 📝 License

Copyright © 2022 [Arie Syukron](https://github.com/syukronarie).<br />
This project is [MIT](https://github.com/syukronarie/@omegion1npm/libero-delectus-laboriosam/blob/main/LICENSE) licensed.

happy coding!
