# The <a href="http://moremicromodules.org"><img height="32" src="http://moremicromodules.org/mmm.png" alt="MMM"></a> [Module Guide](http://module.guide)

How to create a module/package/library in any programming language.

* [How to Structure Code and Publish a Module](#how-to-structure-code-and-publish-a-module)
* [How to Write and Run a Unit Test](#how-to-write-and-run-a-unit-test)

## How to Structure Code and Publish a Module

### JavaScript

The package manager situation can be confusing at the beginning. Most modules are published on [npmjs.com](http://npmjs.com/), but some are served directly from [github.com](https://github.com). To complicate things even further, there are different module systems, which describe how to access the code. Here are three different ways how you can publish your code. If you are doing server-side node.js programming, pick option one (NPM and CommonJS). If you are doing front-end programming, and you are unsure which one to use, option two (JSPM and ES6 moudles) is a good choice. Option three (Bower and browser globals) is simple to use, but disregarded in large parts of the JavaScript community. A very detailed description of current JavaScript package managers and module systems can found in [this blog arcticle by Nolan Lawsons](http://nolanlawson.com/2015/10/19/the-struggles-of-publishing-a-javascript-library/)!

* [JAVASCRIPT + NPM + COMMONJS](https://github.com/micromodules/guides/blob/master/MODULES/JAVASCRIPT-NPM-COMMONJS.md) (node.js style)
* [JAVASCRIPT + JSPM + ES6 MODULES](https://github.com/micromodules/guides/blob/master/MODULES/JAVASCRIPT-JSPM-ES6.md) (future proof style)
* [JAVASCRIPT + BOWER + BROWSER GLOBALS](https://github.com/micromodules/guides/blob/master/MODULES/JAVASCRIPT-BOWER-GLOBALS.md) (almost no package manager style)

### Ruby

The usual way to publish Ruby modules is using [rubygems.org](https://rubygems.org):

* [RUBY + RUBYGEMS](https://github.com/micromodules/guides/blob/master/MODULES/RUBY-RUBYGEMS.md)


## How to Write and Run a Unit Test

### Ruby

While using [RSpec](http://rspec.info/) is quasi-standard in the Ruby community, [minitest](https://github.com/seattlerb/minitest) is getting more attention lately, and is even [bundled in Ruby's standard library](https://github.com/ruby/ruby/blob/v2_2_3/gems/bundled_gems#L3).

* [RUBY: RSPEC](https://github.com/micromodules/guides/blob/master/TESTS/RUBY-RSPEC.md) (TBD)
* [RUBY: MINITEST](https://github.com/micromodules/guides/blob/master/TESTS/RUBY-MINITEST.md) (TBD)
