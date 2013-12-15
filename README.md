###Lanching Sinatra app to Heroku
- Create your Sinatra application
- Create your config.ru file
	- this is the instructions to heroku on how to start your application
- Create your Gemfile
	- this is where you list your required gems and ruby version
- bundle
	- this makes a .lock file which lists ALL of your applications dependencies
- Make your applications folder a git repo 
- heroku create
	- this tells heroku to prepare a repo for you
	- this adds a remote to your git repo called `heroku`
- Push up to heroku!

--- 

##How-to:

---
####in terminal...
```bash

mkdir my_sinatra_heroku_app
cd my_sinatra_heroku_app
touch main.rb
touch config.ru
touch Gemfile

```

---

####main.rb
```ruby

require 'bundler/setup'
Bundler.require(:default)

get '/' do
	"Your site has launched!!!"	
end

```

---

####config.ru
```javasoft

require './main'
run Sinatra::Application

```

---

####Gemfile
```ruby

source "https://rubygems.org"
ruby "2.0.0"
gem 'sinatra'

```

---

####in terminal...
```bash

bundle
git init
git add -A
git commit -m "Init Commit"
heroku login
heroku create
git push heroku master

```
