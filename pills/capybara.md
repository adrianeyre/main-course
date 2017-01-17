# Capybara Setup


## Install Gems
```
$ gem install "capybara"

$ gem install "selenium-webdriver"

$ brew install geckodriver
```

## Firefox
```
Download latest version of Firefox
```

## Test Capybara in IRB or PRY
```ruby
$ require 'capybara'
=> true
$ require 'selenium-webdriver'
=> true
$ require 'capybara/dsl'
=> true
$ include Capybara::DSL
=> including Capybara::DSL in the global scope is not recommended!
$ Capybara.default_driver = :selenium
=> :selenium
$ visit 'http://capybaraworkout.herokuapp.com'
=> Opens website in Firefox
$ click_link 'Start Workout!'
=> Starts workout
```
