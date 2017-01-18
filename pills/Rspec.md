# Ruby Testing Framework (Rspec)

[Setting up Rspec](#RspecSetup) | [Setting up Rspec for Sanatra](#SinatraSetup) | [Gems Required](#Gems) <br>
[Rspec Standard Layout](#Layout) | [Expect Syntax](#Expect) | [Week 3](#Week3) | [Week 4](#Week4) |

## Setting up Rspec
## <a name="RspecSetup">Setting up Rspec</a>
```shell
$ rspec --init
```
This creates `.rspec` and `spec/spec_helper.rb` files.

## <a name="SinatraSetup">Setting up Rspec for Sanatra</a>
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

## <a name="Gems">Gems required</a>
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

## <a name="Layout">Rspec Standard Layout</a>
```ruby
describe <Class Name> do
  describe '#<Method Name>' do
    context 'In what context' do
      it 'does something' do
        expect....
      end
    end
  end
end
```

## <a name="Expect">Expect Syntax</a>
