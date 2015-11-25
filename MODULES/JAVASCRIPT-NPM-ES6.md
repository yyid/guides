# JAVASCRIPT + NPM + ES6 MODULES

## Description

This guide describes a method to package JavaScript libraries using future [ES6-sytle  modules](http://www.2ality.com/2014/09/es6-modules-final.html). These are not directly supported by browsers or [node.js](http://nodejs.org/), but there are ways to nevertheless load ES6 modules.

A comfortable way to do so is to use [JSPM](http://jspm.io) as your application's package manager. JSPM does not host packages directly, but wraps around [npm](https://www.npmjs.com/) and [GitHub](http://github.com/). Under the hood, JSPM uses [System.js](https://github.com/systemjs/systemjs), which handles the actual module loading.

## How to Package a Module

**Please note:** Publishing ES6 modules is not so common yet and practices vary so please expect future changes in this section.

*Replace `mmm` with your module's name.*

### Recommended File Structure

    .
    ├── dist
    │   └── mmm.js
    ├── src
    │   ├── mmm.js
    │   └── otherSourceFile.js
    └── package.json

You should also add information and documentation to your module, by adding a `README.md`, a `LICENSE.txt`, and a `CHANGELOG.md` file.

### `package.json`

The `package.json` file contains your module's meta data. You can interactively create one using `$ npm init`

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
  "main": "src/index.js",
  "dependencies": {
  },
  "devDependencies": {
  },
  "license": "MIT"
}
```

TBD: Describe how to add dependencies

###

## How to Publish a Module

[Documentation](https://docs.npmjs.com/getting-started/publishing-npm-packages)

TBD: Register

In the module directory run:

```shell
$ npm publish
```

## Resources

TBD
