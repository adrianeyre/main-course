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

## File: .coveralls.yml
```
8. Copy service_name and a repo_token into the coveralls.yml file
```

## Gemfile
```
gem 'coveralls', require: false
```

## File: spec/spec_helper.rb
```
require 'coveralls'
Coveralls.wear!
```

## Make a Rakefile
```
$ atom Rakefile
```

## Paste below into Rakefile
```
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new :spec
task default: [:spec]
```

## Terminal
```shell
$ bundle
$ coveralls report
```
