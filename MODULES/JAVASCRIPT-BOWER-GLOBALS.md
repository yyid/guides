# JAVASCRIPT + BOWER + BROWSER GLOBALS

## Description

This is a very lightweight way to package up a module. Instead of uploading your code to [npm](https://www.npmjs.com/), you push it to a [git repositoy](https://en.wikipedia.org/wiki/Git_%28software%29) (typically on [GitHub](http://github.com)) and register it with [Bower](http://bower.io/). Using "browser globals" refers to neither using CommonJS/AMD/ES6 modules, but using a "non-magic" global JavaScript variable.

**Please note:** Bower defines a way to *distribute your code published on github.com*, you can also push your code to npm at the same time. Also, it does not make any assumption about your module system, so instead of using browser globals (as shown in this guide), you could also use [CommonJS](https://webpack.github.io/docs/commonjs.html), [AMD](http://requirejs.org/docs/whyamd.html) or [ES6 modules](http://www.2ality.com/2014/09/es6-modules-final.html) with Bower. 

In order to use Bower, you must first [install node and then bower via npm: `$ npm install -g bower`](http://bower.io/#install-bower)

## How to Package a Module

### Recommended File Structure

*Replace `mmm` with your module's name.*

    .   
    ├── bower.json
    └── mmm.js

You should also add information and documentation to your module, by adding a `README.md`, a `LICENSE.txt`, and a `CHANGELOG.md` file.

#### `bower.json`

The `bower.json` file contains your module's meta data. You can interactively create a new one in the current folder using `$ bower init`

```json
{
  "name": "mmm",
  "authors": [
    "Jane Doe <mail@moremicromodules.org>",
    "Max Mustermann"
  ],  
  "description": "Description",
  "main": "mmm.js",
  "moduleType": [
    "globals"
  ], 
  "license": "MIT",
  "homepage": "",
  "ignore": [
    "**/.*",
    "node_modules",
    "bower_components"
  ]
}
```

#### `mmm.js`

The following code will make your code available as single global variable:

```javascript
// Wrap everything in a function so that it does not leak variables
(function(global){
  // Activate JavaScript's strict mode
  'use strict';

  var mmm = {
    foo: function foo(){
      console.log('foo');
    },
    bar: function bar(){
      console.log('bar');
    }
  }

  global.mmm = mmm;
})(this);
```

You can also support multiple module systems at once, see [UMD](https://github.com/umdjs/umd/) for instructions to do so.

## How to Publish a Module

Make your code available online, for example, by pushing it to a [repository on github](https://help.github.com/articles/create-a-repo/). Make sure it has [git tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging) representing the respective versions.

Then register it with:

    $ bower register mmm git://github.com/username/mmm.git
