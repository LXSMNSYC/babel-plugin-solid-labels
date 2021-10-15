
# ![banner](https://github.com/LXSMNSYC/babel-plugin-solid-labels/blob/main/images/banner.png?raw=true)

[![NPM](https://img.shields.io/npm/v/babel-plugin-solid-labels.svg)](https://www.npmjs.com/package/babel-plugin-solid-labels) [![JavaScript Style Guide](https://badgen.net/badge/code%20style/airbnb/ff5a5f?icon=airbnb)](https://github.com/airbnb/javascript)

<p align="center">
  <img
    src="https://github.com/LXSMNSYC/babel-plugin-solid-labels/blob/main/images/example.png?raw=true"
    alt="Example"
    style="width: 80%; height: auto;"
  />
</p>

## Install

```bash
npm install babel-plugin-solid-labels
```

```bash
yarn add babel-plugin-solid-labels
```

```bash
pnpm add babel-plugin-solid-labels
```

## Features

- 🏷 Labels: Turn labels into SolidJS utility calls!
- 💬 Comments: Turn comments into SolidJS utility calls, too!
- ⏱ Compile-time Functions: Use functions that are evaluated during compile-time!
- 📦 Auto Imports: No need to import SolidJS utilities, explicitly!
- 🤝 JS and TS Friendly!

## Usage

- [Labels](https://github.com/LXSMNSYC/babel-plugin-solid-labels/tree/main/docs/labels.md)
[![Open in CodeSandbox](https://img.shields.io/badge/Open%20in-CodeSandbox-blue?style=flat-square&logo=codesandbox)](https://codesandbox.io/s/github/LXSMNSYC/babel-plugin-solid-labels/tree/main/examples/vite-example-comments)
- [Comments](https://github.com/LXSMNSYC/babel-plugin-solid-labels/tree/main/docs/comments.md)
[![Open in CodeSandbox](https://img.shields.io/badge/Open%20in-CodeSandbox-blue?style=flat-square&logo=codesandbox)](https://codesandbox.io/s/github/LXSMNSYC/babel-plugin-solid-labels/tree/main/examples/vite-example-comments)
- [Compile-Time Functions](https://github.com/LXSMNSYC/babel-plugin-solid-labels/tree/main/docs/ctf.md)
[![Open in CodeSandbox](https://img.shields.io/badge/Open%20in-CodeSandbox-blue?style=flat-square&logo=codesandbox)](https://codesandbox.io/s/github/LXSMNSYC/babel-plugin-solid-labels/tree/main/examples/vite-example-ctf)

### Typescript

`<any file>.d.ts`

```ts
/// <reference types="babel-plugin-solid-labels" />
```

### Babel

`.babelrc`

```json
{
  "plugins": [
    ["babel-plugin-solid-labels", { "dev": false }]
  ]
}
```

### Vite

`vite-plugin-solid`

```js
// vite.config.js
import { defineConfig } from 'vite';
import solidPlugin from 'vite-plugin-solid';
import solidLabels from 'babel-plugin-solid-labels';

export default defineConfig({
  plugins: [
    solidPlugin({
      babel: {
        plugins: [
          [solidLabels, { dev: process.env.NODE_ENV !== 'production' }]
        ],
      },
    }),
  ],
});
```

`solid-start`

```js
// vite.config.js
import { defineConfig } from 'vite';
import solidStart from 'solid-start';
import solidLabels from 'babel-plugin-solid-labels';

export default defineConfig({
  plugins: [
    solidStart({
      babel: {
        plugins: [
          [solidLabels, { dev: process.env.NODE_ENV !== 'production' }]
        ],
      },
    }),
  ],
});
```

## Limitations

- Detecting shadowed identifier for `signal` and `memo`.

## License

MIT © [lxsmnsyc](https://github.com/lxsmnsyc)
