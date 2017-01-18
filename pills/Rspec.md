# Ruby Testing Framework (Rspec)

[Setting up Rspec](#RspecSetup) | [Setting up Rspec for Sanatra](#SinatraSetup) | [Gems Required](#Gems) <br>
[Rspec Standard Layout](#Layout) | [Expect Syntax](#Expect) | [Before Block](#Before) | [Subject, Doubles and Stubs](#Subject)

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
```ruby
expect(subject).to receive(:<method name>)
expect(subject).to receive(:<method name>).and_return true
expect(subject.somemethod).to eq 'something'
expect(subject.somemethod).to > 1
expect(subject.somemethod).to < 1
expect(subject.somemethod).to include 'something'
expect(subject.somemethod).to be_between(minimum, maximum).inclusive
expect(subject.somemethod).to be_between(minimum, maximum).exclusive
expect(subject.somemethod).to match(/expression/)
expect(subject.somemethod).to start_with expected
expect(subject.somemethod).to end_with expected
expect(subject.somemethod).to exist
expect(subject.somemethod).to exist(*args)
expect(subject.somemethod).to be_instance_of(expected)
expect(subject.somemethod).to be_kind_of(expected)
expect(subject.somemethod).to respond_to(expected)

expect {subject.somemethod}.to raise_error 'error'
expect {subject.somemethod}.not_to raise_error
```

## <a name="Before">Before Block</a>
```ruby
before do
  allow(subject).to receive(:<method name>).and_return true
end
```

## <a name="Subject">Subject, Doubles and Stubs</a>
```ruby
subject(:<Class Name>) { described_class.new }
let(:<Double Name>) { double :<Class Name>, method: result}
variable = subject.instance_variable_get(:@variable)
```
