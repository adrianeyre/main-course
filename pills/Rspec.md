# Ruby Testing Framework (Rspec)

## Setting up Rspec
```shell
$ rspec --init
```
This creates `.rspec` and `spec/spec_helper.rb` files.

## Setting up Rspec for Sanatra
```shell
$ rspec-sinatra init --app <App Name> <Ruby Filename>
```
This creates `<Ruby Filename>` and `config.ru` files.

### File: <Ruby Filename>
```ruby
require 'sinatra/base'

class <App Name> < Sinatra::Base
  get '/' do
    'Hello Battle!'
  end

  # start the server if ruby file executed directly
  run! if app_file == $0
end
```

## Gems required
* Rspec
```ruby
gem 'rspec'
```

Rspec-Sinatra
```ruby
gem 'rspec'
gem 'sinatra'
gem 'rspec-sinatra'
gem 'capybara'
gem 'selenium-webdriver'
```
