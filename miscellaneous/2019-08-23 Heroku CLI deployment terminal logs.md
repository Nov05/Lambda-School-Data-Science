2019-08-03 

# Heroku CLI Deployment Terminal Logs   

1. Install CLI in Linux (Google Colab)  
```!curl https://cli-assets.heroku.com/install.sh | sh```

2. Tunnel Jupyter Notebook local port `8888` to the Internet
```
# Install ngrok
!wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip
!unzip ngrok-stable-linux-amd64.zip
%cd /content
get_ipython().system_raw('./ngrok http 8888 &')
!curl -s http://localhost:4040/api/tunnels | python3 -c \
"import sys, json; print(json.load(sys.stdin)['tunnels'][0]['public_url'])"
!jupyter notebook
# click on the ngrok link to open a jupyter notebook
# e.g. https://19962c4d.ngrok.io/
```

3. In the Jupyter Notebook, click on the `New` button in the upper right corner, then select `Terminal`

4. In the terminal web page, follow the Heroku deployment instructions. you will be able to click on the Heroku login link and login from the terminal, just like most local terminals.

5. Before this, you can also install `pipenv` in Google Colab, control dependencies there, generate requirements.txt file, etc. Or you can save all files on [**Google Drive**](https://drive.google.com/open?id=1063bvSI7m4vfHTibPVktuWMfgNCShoNU), so they won't be removed when resetting all the runtimes. **Anyway, everything was done in Google Colab.** All examples are in this [**Colab Notebook**](https://colab.research.google.com/drive/1MJa6o8mf2vxxnpxRbCmlRcbeYSkDnFSP?authuser=1#scrollTo=YIzu8ls5Csq0&line=4&uniqifier=1). 

6. Visit the app at https://iris-app-20190823.herokuapp.com/   

7. `/content` is Google Colab default folder  

### Terminal Logs

```
root@2dc61bb7537d:/content# heroku loginheroku: Press any key to open up the browser to login or q to exit:
 ›   Error: quit
root@2dc61bb7537d:/content# cd irisapp
root@2dc61bb7537d:/content/irisapp# git init
Initialized empty Git repository in /content/irisapp/.git/
root@2dc61bb7537d:/content/irisapp# heroku git:remote -a iris-app-20190823
heroku: Press any key to open up the browser to login or q to exit:
Opening browser to https://cli-auth.heroku.com/auth/browser/b805f68a-fb58-4994-bdb3-360e60ece2db
 ›   Warning: Cannot open browser.
heroku: Waiting for login... ⢿
Logging in... done
set git remote heroku to https://git.heroku.com/iris-app-20190823.git
root@2dc61bb7537d:/content/irisapp# git add .
root@2dc61bb7537d:/content/irisapp# git commit -m "2019-08-23 first commit"

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'root@2dc61bb7537d.(none)')
root@2dc61bb7537d:/content/irisapp# git config --global user.email "xxx@xxx.com"
root@2dc61bb7537d:/content/irisapp# git config --global user.name "xxx"
root@2dc61bb7537d:/content/irisapp# git commit -m "2019-08-23 first commit"
[master (root-commit) 78cb083] 2019-08-23 first commit
 9 files changed, 324 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 Pipfile
 create mode 100644 Pipfile.lock
 create mode 100644 Procfile
 create mode 100644 app.py
 create mode 100644 model.pkl
 create mode 100644 requirements.txt
 create mode 100644 templates/index.html
 create mode 100644 templates/result.html
root@2dc61bb7537d:/content/irisapp# git push heroku master
Counting objects: 12, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (11/11), done.
Writing objects: 100% (12/12), 7.08 KiB | 7.08 MiB/s, done.
Total 12 (delta 0), reused 0 (delta 0)
remote: Compressing source files... done.
remote: Building source:
remote:
remote: -----> Python app detected
remote: -----> Installing python-3.6.8
remote: -----> Installing pip
remote: -----> Installing dependencies with Pipenv 2018.5.18…
remote:        Installing dependencies from Pipfile.lock (0140e5)…
remote: -----> Installing SQLite3
remote: -----> Discovering process types
remote:        Procfile declares types -> web
remote:
remote: -----> Compressing...
remote:        Done: 114.1M
remote: -----> Launching...
remote:        Released v3
remote:        https://iris-app-20190823.herokuapp.com/ deployed to Heroku
remote:
remote: Verifying deploy... done.
To https://git.heroku.com/iris-app-20190823.git
 * [new branch]      master -> master
root@2dc61bb7537d:/content/irisapp#
```
