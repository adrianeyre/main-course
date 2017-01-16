# Capybara Setup


Install Gems
```
$ gem install "capybara"

$ gem install "selenium-webdriver"
```

Install Geckodriver
```
Goto https://github.com/mozilla/geckodriver/releases

Download latest version

Unzip the file and put it in your projects folder

Type:  export PATH=$PATH:/Users/AdrianEyre/Projects (Geckodriver file location)

Run the "geckodriver" file
```

Firefox
```
Download latest version of Firefox

Open Firefox
```

Test Capybara in IRB or PRY
```ruby
$ require 'capybara'
=> true
$ require 'selenium-webdriver'
=> true
$ require 'capybara/dsl'
=> true
$ include Capybara::DSL
=> including Capybara::DSL in the global scope is not recommended!
Capybara.default_driver = :selenium
=> :selenium
visit 'http://capybaraworkout.herokuapp.com'
=> Opens website in Firefox
click_link 'Start Workout!'
=> Starts workout
```
