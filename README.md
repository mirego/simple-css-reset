simple-css-reset
================

[![Build Status](https://travis-ci.org/mirego/simple-css-reset.svg?branch=master)](https://travis-ci.org/mirego/simple-css-reset)
[![npm](https://img.shields.io/npm/v/simple-css-reset.svg)](https://www.npmjs.com/package/simple-css-reset)

A simple, no-nonsense CSS reset stylesheet.

## Installation

```bash
$ npm install --save simple-css-reset
```

## Usage

### Ember.js

You need the `ember-cli-node-assets` package to be able to import the CSS file into your application. Then you need to add the reset file to the `ember-cli` build file.

```bash
$ npm install --save-dev ember-cli-node-assets
```

```js
// ember-cli-build.js
module.exports = function(defaults) {
  const app = new EmberApp(defaults, {
    nodeAssets: {
      'simple-css-reset': {
        import: ['reset.css']
      }
    }
  });
};
```

### Webpack

Assuming you have properly installed and configured [CSS loader](https://github.com/webpack-contrib/css-loader), you can simply require the `reset.css` file within the entry point of your app.

```bash
$ npm install --save-dev css-loader
```

```js
// index.js
import 'simple-css-reset/reset.css';
```
