# @violentmonkey/dom

[![NPM](https://img.shields.io/npm/v/@violentmonkey/dom.svg)](https://npm.im/@violentmonkey/dom)
![License](https://img.shields.io/npm/l/@violentmonkey/dom.svg)

Use JSX for HTML elements.

Based on [@gera2ld/jsx-dom](https://github.com/gera2ld/jsx-dom).

## Usage

First, include `@violentmonkey/dom` as a dependency:

```js
// ...
// @require https://cdn.jsdelivr.net/npm/@violentmonkey/dom@1
// ...
```

Then you can use `VM.createElement` directly:

```js
document.body.appendChild(VM.createElement('div', {}, 'hello'));
```

Or use with JSX and bundlers, for example:

```js
// .babelrc.js
{
  plugins: [
    // JSX
    ['@babel/plugin-transform-react-jsx', {
      pragma: 'VM.createElement',
      pragmaFrag: 'VM.Fragment',
    }],
  ],
}
```

```js
document.body.appendChild(<div>hello</div>);
```

To initialize a project for userscript with JSX support, try [generator-userscript](https://github.com/violentmonkey/generator-userscript):

```sh
$ mkdir my-script
$ cd my-script
$ npx -p https://github.com/violentmonkey/generator-userscript.git -p yo yo @violentmonkey/userscript
```

## API

### VM.createElement

`VM.createElement(tag, props, ...children)`

### VM.Fragment
