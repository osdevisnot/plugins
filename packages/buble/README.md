[cover]: https://codecov.io/gh/rollup/plugins/buble/branch/master/graph/badge.svg
[cover-url]: https://codecov.io/gh/rollup/plugins
[size]: https://packagephobia.now.sh/badge?p=@rollup/plugin-buble
[size-url]: https://packagephobia.now.sh/result?p=@rollup/plugin-buble
[tests]: https://img.shields.io/circleci/project/github/rollup/plugins.svg
[tests-url]: https://circleci.com/gh/rollup/plugins

[![tests][tests]][tests-url]
[![cover][cover]][cover-url]
[![size][size]][size-url]
[![libera manifesto](https://img.shields.io/badge/libera-manifesto-lightgrey.svg)](https://liberamanifesto.com)

# @rollup/plugin-buble

🍣 A Rollup which converts ES2015+ code with the Bublé compiler.

## Requirements

This plugin requires an [LTS](https://github.com/nodejs/Release) Node version (v8.0.0+) and Rollup v1.20.0+.

## Install

Using npm:

```console
npm install @rollup/plugin-buble --save-dev
```

## Usage

Create a `rollup.config.js` [configuration file](https://www.rollupjs.org/guide/en/#configuration-files) and import the plugin:

```js
import buble from '@rollup/plugin-buble';

export default {
  input: 'src/index.js',
  output: {
    dir: 'output',
    format: 'cjs'
  },
  plugins: [buble()]
};
```

Then call `rollup` either via the [CLI](https://www.rollupjs.org/guide/en/#command-line-reference) or the [API](https://www.rollupjs.org/guide/en/#javascript-api).

## Options

### `transforms`

Type: `Object`
Default: `{ modules: false }`

Specifies additional [transform options](https://buble.surge.sh/guide/) for the Bublé compiler

### `exclude`

Type: `String` | `Array[...String]`
Default: `null`

A [minimatch pattern](https://github.com/isaacs/minimatch), or array of patterns, which specifies the files in the build the plugin should _ignore_. By default no files are ignored.

### `include`

Type: `String` | `Array(String)`
Default: `null`

A [minimatch pattern](https://github.com/isaacs/minimatch), or array of patterns, which specifies the files in the build the plugin should operate on. By default all files are targeted.

## Meta

[CONTRIBUTING](./.github/CONTRIBUTING.md)

[LICENSE (MIT)](./LICENSE)
