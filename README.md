
# Redmine 3.4 on Heroku


## How to deploy [Redmine] on [Heroku]

1. Make sure you have the [Heroku Toolbelt] installed.
2. Click this button and follow the instructions: <BR/> [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
3. After you have an instance running on Heroku, run these commands in your terminal.

```
$ heroku git:clone -a <YOUR-APP-NAME>
$ cd <YOUR-APP-NAME>
$ heroku run rake redmine:load_default_data
$ heroku run rake redmine:plugins:migrate RAILS_ENV=production
```

You can now log into your Redmine installation using the initial user account (username: `admin`,  password: `admin`).

