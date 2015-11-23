# [module.guide](http://module.guide)

<img width="200" src="http://moremicromodules.org/mmm.png" alt="MMM">

## How to Structure Code and Publish a Module

### JavaScript

The package manager situation can be confusing at the beginning. Most modules are published on [npmjs.com](http://npmjs.com/), but some only live on [github.com](https://github.com). To complicate things, there are different module systems, which describe how to access the code. Here are three different ways how you can publish your code. If you are unsure, which one to use, pick option three (JSPM + ES6). A good article to understand (...)

* [JAVASCRIPT + NPM + COMMONJS](https://github.com/micromodules/guides/blob/master/MODULES/JAVASCRIPT-NPM-COMMONJS.md) (node.js style)
* [JAVASCRIPT + BOWER + BROWSER GLOBALS](https://github.com/micromodules/guides/blob/master/MODULES/JAVASCRIPT-BOWER-GLOBALS.md) (almost no package manager style)
* [JAVASCRIPT + JSPM + ES6 MODULES](https://github.com/micromodules/guides/blob/master/MODULES/JAVASCRIPT-JSPM-ES6.md) (future proof style)

### Ruby

The usual way to publish Ruby modules is using [rubygems.org](https://rubygems.org):

* [RUBY + RUBYGEMS](https://github.com/micromodules/guides/blob/master/MODULES/RUBY-RUBYGEMS.md)


## How to Write and Run a Unit Test

### Ruby

While using [RSpec](...) is quasi-standard in the Ruby community, [minitest] is getting more attention lately, and is even bundled in Ruby's standard library.

* [RUBY: RSPEC](https://github.com/micromodules/guides/blob/master/TESTS/RUBY-RSPEC.md) (TBD)
* [RUBY: MINITEST](https://github.com/micromodules/guides/blob/master/TESTS/RUBY-MINITEST.md) (TBD)
