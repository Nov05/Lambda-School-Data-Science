2019-08-01  

Dash App on Heroku  
https://hours-estimate.herokuapp.com/  
GitHub Repo   
https://github.com/Nov05/DS-Unit-2-Sprint-4-Project  

1. navigate: Heroku > `hours-estimate`(or your own app name) > Activity > View build log  

```
-----> Deleting 2 files matching .slugignore patterns.
-----> Python app detected
-----> Installing python-3.7.3
-----> Installing pip
-----> Installing dependencies with Pipenv 2018.5.18…
       Installing dependencies from Pipfile.lock (03dc5a)…
       Ignoring appnope: markers 'sys_platform == "darwin"' don't match your environment
       You are using pip version 9.0.2, however version 19.2.1 is available.
       You should consider upgrading via the 'pip install --upgrade pip' command.
-----> Installing SQLite3
-----> Discovering process types
       Procfile declares types -> web
-----> Compressing...
       Done: 129.7M
-----> Launching...
       Released v3
       https://hours-estimate.herokuapp.com/ deployed to Heroku
```

2. visit the app at `https://hours-estimate.herokuapp.com/`  

3. if you saw error and would need to check the logs
* download and install the Heroku Command Line (CLI)  
https://devcenter.heroku.com/articles/heroku-cli  
* for Windows 10, type `cmd` in the Stat Search Menu to launch the Commond Prompt
* type `heroku -a hours-estimate` (or your own app name)  


