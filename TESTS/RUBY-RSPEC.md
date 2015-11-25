# RUBY: Testing with RSPEC

## Description

[RSpec](http://rspec.info/) is the most popular option for testing in Ruby land. Before testing your gem with RSpec, you need to add it to the `*.gemspec` file:

```ruby
gem.add_development_dependency 'rspec', '~> 3.4'
```

## Recommended File Structure

    .
    ├── <other module files>
    ├── .rspec
    ├── Gemfile
    └── spec
        ├── mmm_spec.rb
        └── other_module_spec.rb

TODO explain files, Gemfile optional

## How to Write a Unit Test

TODO

## How to Execute the Test Suite

Run everything:

```ruby
$ rspec
```

To only run individual files:

```ruby
$ rspec spec/other_module_spec.rb
```

TODO show example output