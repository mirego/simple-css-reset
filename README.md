<div align="center">
  <img src="https://user-images.githubusercontent.com/11348/55351996-cdb7af80-548d-11e9-8a01-7488378a9875.png" width="600" />
  <p><br />A simple, no-nonsense CSS reset stylesheet to use as an NPM dependency.</p>
  <p>
    <a href="https://travis-ci.com/mirego/simple-css-reset"><img src="https://travis-ci.com/mirego/simple-css-reset.svg?branch=master" />
  </a>
    <a href="https://www.npmjs.com/package/simple-css-reset"><img src="https://img.shields.io/npm/v/simple-css-reset.svg" /></a>
  </p>
</div>

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


## License

`simple-css-reset` is © 2014-2019 [Mirego](http://www.mirego.com) and may be freely distributed under the [New BSD license](http://opensource.org/licenses/BSD-3-Clause).  See the [`LICENSE.md`](https://github.com/mirego/simple-css-reset/blob/master/LICENSE.md) file.

The reset logo is based on [this lovely icon by Hali Gali Harun](https://thenounproject.com/term/reset/415758), from The Noun Project. Used under a [Creative Commons BY 3.0](http://creativecommons.org/licenses/by/3.0/) license.

## About Mirego

[Mirego](https://www.mirego.com/en) is a team of passionate people who believe that work is a place where you can innovate and have fun. We're a team of [talented people](https://life.mirego.com/en) who imagine and build beautiful Web and mobile applications. We come together to share ideas and [change the world](http://www.mirego.org/en).

We also [love open-source software](https://open.mirego.com) and we try to give back to the community as much as we can.
