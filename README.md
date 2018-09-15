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

When using Ember 2.15 and up, simply add the css file to your build using `app.import`.
```js
// ember-cli-build.js
module.exports = function(defaults) {
  const app = new EmberApp(defaults, {
   // Add options here
  });

  app.import('node_modules/simple-css-reset/reset.css');

  return app.toTree();
};
```

When using Ember 2.14 and below, you need the `ember-cli-node-assets` package to be able to import the CSS file into your application. Then you need to add the reset file to the `ember-cli` build file.

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


## License

`simple-css-reset` is © 2014-2017 [Mirego](http://www.mirego.com) and may be freely distributed under the [New BSD license](http://opensource.org/licenses/BSD-3-Clause).  See the [`LICENSE.md`](https://github.com/mirego/simple-css-reset/blob/master/LICENSE.md) file.

## About Mirego

[Mirego](https://www.mirego.com/en) is a team of passionate people who believe that work is a place where you can innovate and have fun. We're a team of [talented people](https://life.mirego.com/en) who imagine and build beautiful Web and mobile applications. We come together to share ideas and [change the world](http://www.mirego.org/en).

We also [love open-source software](https://open.mirego.com) and we try to give back to the community as much as we can.
