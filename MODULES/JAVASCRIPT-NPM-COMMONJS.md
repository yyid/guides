# JAVASCRIPT + NPM + COMMONJS

## Description

This is the standard way to package node (server-side) modules. The package manager of choice is [npm](https://www.npmjs.com/). The format you structure your code in is called [CommonJS](https://webpack.github.io/docs/commonjs.html).

You can also use npm for client-side code, but you will need a tool that handles the module loading in the browser and/or packages all code into a single bundle file. Such tools include:

- [Browserify](http://browserify.org/)
- [Webpack](http://webpack.github.io/)
- [System.js](https://github.com/systemjs/systemjs)

## How to Package a Module

*Replace `mmm` with your module's name.*

### Recommended File Structure

    .
    ├── index.js
    ├── lib
	  │   └── otherSourceFile.js
    └── package.json


You should also add information and documentation to your module, by adding a `README.md`, a `LICENSE.txt`, and a `CHANGELOG.md` file.

### `package.json`

The `package.json` file contains your module's meta data. You can interactively create a new one in the current folder using `$ npm init`

[Documentaton](https://docs.npmjs.com/files/package.json)

```json
{
  "name": "mmm",
  "version": "0.1.0",
  "description": "Description",
  "homepage": "https://github.com/micromodules/meetup",
  "repository": {
    "type": "git",
    "url": "git://github.com/micromodules/meetup.git"
  },
  "author": {
    "name": "Jane Doe",
    "email": "mail@moremicromodules.org",
    "url": "http://moremicromodules.org"
  },
  "keywords": [
    "micro",
    "module"
  ],
  "main": "index.js",
  "dependencies": {
  },
  "devDependencies": {
  },
  "license": "MIT"
}
```

TBD: Describe how to add dependencies

### `index.js`

This is the entry point to your code. Use `require()` to load packaged dependencies or local source files. Use `module.export` to declarce the public interface of your module (this can be any kind of JavaScript object);

```javascript
// Activate JavaScript's strict mode
'use strict';

// Require your dependencies, for example:
// require('extern-dependency');
// require('./lib/otherSourceFile');

function mmm(){
  console.log('More Micro Modules');
);

module.exports = mmm;
```

The usage of your module would then be:

```javascript
var mmm = require('mmm');
mmm(); // => 'More Micro Modules'
```

## How to Publish a Module

TBD: Register

In the module directory run:

```shell
$ npm publish
```
