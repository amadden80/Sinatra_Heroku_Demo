###Lanching to Sinatra app to Heroku


```bash

mkdir my_sinatra_heroku_app
cd my_sinatra_heroku_app
touch main.rb
touch config.ru
touch Gemfile

```

####main.rb
```ruby

require 'sinatra'

get '/' do
	"Your site has launched!!!"	
end

```

####config.ru
```javasoft

require './main'
run Sinatra::Application

```


####Gemfile
```ruby

source "https://rubygems.org"
ruby "1.9.3"
gem 'sinatra', '1.4.3'

```

---

```bash

bundle
git init
git add -A
git commit -m "Init Commit"
heroku login
heroku create
git push heroku master

```
