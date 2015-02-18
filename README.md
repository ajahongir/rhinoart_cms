# Rhinoart

Rhinoart is a admin engine system. This a CMS backend

## Installation:

``` ruby
# Gemfile for Rails 4
gem 'rhinoart', git: 'https://github.com/kostyakch/rhinoart_cms.git'
```

## Basic rhinoart use

### Add in Your Gemfile line like this:
``` ruby
gem 'rhinoart', github: 'kostyakch/rhinoart_cms'
```

### In routes.rb add:
``` ruby
# Admin URLs
mount Rhinoart::Engine, at: "/admin"
```

After it:

``` ruby
$ rake db:create
$ rake rhinoart:install:migrations
$ rake db:migrate

#and
$ rake db:populate
```
Now You cat login: http://0.0.0.0:3000/admin
login: admin@test.com
password: admin

You may need to change line in Your app config/environments/development.rb
``` ruby
config.eager_load = true
```
