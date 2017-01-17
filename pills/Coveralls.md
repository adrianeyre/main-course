# Coveralls Setup

## Set up a Coveralls account
```
Go to: https://coveralls.io

Sign up for the free account.

Add your Github account details (and authorise) and wait for your repos to refresh

Click on your Github username on the right hand side and click Options > Filter. This will display your repos.

Click “ON” on the repo you want to test, then click “DETAILS” to the right of the repo name.
```

## Terminal
```shell
$ atom .coveralls.yml
```

## .coveralls.yml
```
8. Copy service_name and a repo_token into the coveralls.yml file
```

## Gemfile
```
gem 'coveralls', require: false
```

## Terminal
```shell
$ atom spec/spec_helper.rb
```


12. Paste the following in at the very the top of the file (above everything else) & save:
require 'coveralls’
Coveralls.wear!

13. In your terminal, run the command: touch Rakefile

14. Paste the following into the file & save:
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new :spec
task default: [:spec]

15. In the terminal run the command: bundle

16. You should now see your test coverage by running the command: coveralls report

17. To enable coveralls for a new project, just run steps 6 - 16 for the new project.
