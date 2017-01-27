# Sinatra Setup Example

## Install Gems
```ruby
$ gem install "sinatra"
$ gem install "shotgun"
```

## Create Ruby file
```ruby
# Filename: ./app.rb

require "sinatra"
set :session_secret, 'super secret'

get '/cat-form' do
  erb(:cat_form)
end

post '/named-cat' do
  @name = params[:name]
  erb(:index)
end
```

## Input page
```ruby
# Filename: ./views/cat_form.erb

<form action="/named-cat" method="post">
  <font size = 5>Enter your cats name</font>
  <input type="text" name="name">
  <input type="submit" value="Submit">
</form>
```

## Output page
```ruby
# Filename: ./views/index.erb

<h1><center>
<% if @name %>
My name is <%= @name %>
<% else %>
I have no name!
<% end %>
</center></h1>

<div style='border: 3px dashed red'>
  <center><img src='http://bit.ly/1eze8aE'></center>
</div>
```

## Settings
`set :views, File.dirname(__FILE__) + '/views'` = Change views folder

`set :port, 9494` = Set default port

`register Sinatra::Flash` = Set up the Flash feature

`enable :sessions` = enables sessions

`use Rack::MethodOverride` = Allows you to have a hidden text field `name="_method" value="delete"`

`set :session_secret, 'super secret'` = Sets the sessions to super secret
