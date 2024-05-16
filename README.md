# **Bootstraf Ruby Gem**  ![Static Badge](https://img.shields.io/badge/test%20-%20passing%20purple)

[Bootstrap 4](https://bootstrap.com) gem for Ruby on Rails (Sprockets) and Hanami (formerly Lotus).

For Sass versions of Bootstrap 3 and 2 see [bootstrap-sass](https://bootstrap.com) instead.

**Ruby on Rails Note**: Newer releases of Rails have added additional ways for assets to be processed. The ``twbs/bootstrap-rubygem`` is for use with Importmaps or Sprockets, but not Webpack.

## Installation

Please see the appropriate guide for your environment of choice:

* [Ruby on Rails 4+](#a-ruby-on-rails) or other Sprockets environment.
* [Other Ruby frameworks](#b-other-ruby-frameworks) not on Rails.


### a. Ruby on Rails

Add `bootstrap` to your Gemfile:

```ruby
gem 'bootstrap', '~> 5.3.3'
```

This gem requires a Sass engine, so make sure you have **one** of these two gems in your Gemfile:
- [`dartsass-sprockets`](https://github.com/tablecheck/dartsass-sprockets): Dart Sass engine, recommended but only works for Ruby 2.6+ and Rails 5+
- [`dartsass-rails`](https://github.com/rails/dartsass-rails): Dart Sass engine, recommended for Rails projects that use Propshaft
- [`cssbundling-rails`](https://github.com/rails/cssbundling-rails): External Sass engine
- [`sassc-rails`](https://github.com/sass/sassc-rails): SassC engine, deprecated but compatible with Ruby 2.3+ and Rails 4

Also ensure that `sprockets-rails` is at least v2.3.2.

`bundle install` and restart your server to make the files available through the pipeline.

Import Bootstrap styles in `app/assets/stylesheets/application.scss`:

```scss
// Custom bootstrap variables must be set or imported *before* bootstrap.
@import "bootstrap";
```
