2019-07-31  
https://github.com/Nov05/Lambda-School-Data-Science/blob/master/daily%20notes/2019-07-29%20Week%209%20Day%201.md  

# Windows 10  
1. install Anaconda3  
2. Windows Start Menu Search: type and run **"Anaconda Powershell Prompt"**  
3. in the prompt, type the following command:  
* `pip install pipenv` (run only once)     
* `cd <path>` (navigate to the folder where you want to create a local folder for your github repo)
* `git clone https://github.com/rrherr/dash-template` (or some other github repo)  
* `cd dash-template` (navigate to the local folder just created by `git clone <repo>` command)  
* `pipenv install` (run it only once to create a pip virtual environment for this repo/project)  
* `pipenv shell` (run it every time you want to start your pipenv virtual environment)  
* `python run.py` (in the example it contains a Plotly Dash app, so run it every time you want to start the app)   
4. press Ctrl+C to stop running run.py (navigate to the folder and type `pipenv shell` to activate the virtual environment again)  
5. in a new prompt, navigate to the folder and start the same pipenv virtual environment, type `jupyter notebook` to start Jupyter Notebook IDE 
6. you might need to run `pip install scipy` for plotly 4.0.0  
7. run `pipenv run pip freeze > requirements.txt` to generate requirements.txt for app deployment  

<br>

P.S. check your pip virtual environment files  
`C:\Users\*\.virtualenvs\DS-Unit-2-Sprint-4-Project-vhTEmim-\`  

https://thoughtbot.com/blog/how-to-manage-your-python-projects-with-pipenv  
https://github.com/pypa/pipenv/issues/3493  

```
(base) PS C:\Users\*> cd d:/lambdaschool  
(base) PS D:\lambdaschool> cd github  
(base) PS D:\lambdaschool\github> cd..  
(base) PS D:\lambdaschool> pip install pipenv  
Collecting pipenv    
  Downloading https://files.pythonhosted.org/packages/13/b4/3ffa55f77161cff9a5220f162670f7c5eb00df52e00939e203f601b0f579/pipenv-2018.11.26-py3-none-any.whl (5.2MB)
     |████████████████████████████████| 5.2MB 2.2MB/s  
Requirement already satisfied: certifi in c:\users\*\anaconda3\lib\site-packages (from pipenv) (2019.6.16)  
Requirement already satisfied: pip>=9.0.1 in c:\users\*\anaconda3\lib\site-packages (from pipenv) (19.1.1)  
Requirement already satisfied: setuptools>=36.2.1 in c:\users\*\anaconda3\lib\site-packages (from pipenv) (41.0.1)  
Collecting virtualenv-clone>=0.2.5 (from pipenv)  
  Downloading https://files.pythonhosted.org/packages/ba/f8/50c2b7dbc99e05fce5e5b9d9a31f37c988c99acd4e8dedd720b7b8d4011d/virtualenv_clone-0.5.3-py2.py3-none-any.whl
Collecting virtualenv (from pipenv)  
  Downloading https://files.pythonhosted.org/packages/db/9e/df208b2baad146fe3fbe750eacadd6e49bcf2f2c3c1117b7192a7b28aec4/virtualenv-16.7.2-py2.py3-none-any.whl (3.3MB)
     |████████████████████████████████| 3.3MB 6.4MB/s  
Installing collected packages: virtualenv-clone, virtualenv, pipenv  
Successfully installed pipenv-2018.11.26 virtualenv-16.7.2 virtualenv-clone-0.5.3  
(base) PS D:\lambdaschool> git clone https://github.com/Nov05/DS-Unit-2-Sprint-4-Project.git  
Cloning into 'DS-Unit-2-Sprint-4-Project'...  
remote: Enumerating objects: 45, done.  
remote: Counting objects: 100% (45/45), done.  
remote: Compressing objects: 100% (39/39), done.  
remote: Total 45 (delta 12), reused 0 (delta 0), pack-reused 0  
Unpacking objects: 100% (45/45), done.  
(base) PS D:\lambdaschool> ls  

    Directory: D:\lambdaschool

Mode                LastWriteTime         Length Name  
----                -------------         ------ ----   
d-----       2019-07-31  01:17 PM                DS-Unit-2-Sprint-4-Project  
d-----       2019-06-15  01:07 PM                github  

(base) PS D:\lambdaschool> cd ds-unit-2-sprint-4-project  
(base) PS D:\lambdaschool\ds-unit-2-sprint-4-project> ls  

    Directory: D:\lambdaschool\ds-unit-2-sprint-4-project  

Mode                LastWriteTime         Length Name  
----                -------------         ------ ----  
d-----       2019-07-31  01:17 PM                assets  
d-----       2019-07-31  01:17 PM                notebooks  
d-----       2019-07-31  01:17 PM                pages  
-a----       2019-07-31  01:17 PM           1320 .gitignore  
-a----       2019-07-31  01:17 PM             10 .slugignore  
-a----       2019-07-31  01:17 PM           1601 app.py  
-a----       2019-07-31  01:17 PM           1087 LICENSE  
-a----       2019-07-31  01:17 PM            253 Pipfile  
-a----       2019-07-31  01:17 PM          26486 Pipfile.lock  
-a----       2019-07-31  01:17 PM             24 Procfile  
-a----       2019-07-31  01:17 PM             85 README.md  
-a----       2019-07-31  01:17 PM           3774 run.py  

(base) PS D:\lambdaschool\ds-unit-2-sprint-4-project> cat .slugignore  
notebooks/  
(base) PS D:\lambdaschool\ds-unit-2-sprint-4-project> pipenv install  
Creating a virtualenv for this project…  
Pipfile: D:\LambdaSchool\DS-Unit-2-Sprint-4-Project\Pipfile  
Using C:/Users/*/Anaconda3/python.exe (3.7.3) to create virtualenv…  
[=== ] Creating virtual environment...Already using interpreter C:\Users\*\Anaconda3\python.exe  
Using base prefix 'C:\\Users\\*\\Anaconda3'  
New python executable in C:\Users\*\.virtualenvs\DS-Unit-2-Sprint-4-Project-vhTEmim-\Scripts\python.exe  
Installing setuptools, pip, wheel...  
done.  
Running virtualenv with interpreter C:/Users/*/Anaconda3/python.exe  

Successfully created virtual environment!  
Virtualenv location: C:\Users\*\.virtualenvs\DS-Unit-2-Sprint-4-Project-vhTEmim-  
Installing dependencies from Pipfile.lock (03dc5a)…  
Ignoring appnope: markers 'sys_platform == "darwin"' don't match your environment  
Ignoring pexpect: markers 'sys_platform != "win32"' don't match your environment  
Ignoring ptyprocess: markers 'os_name != "nt"' don't match your environment  
  ================================ 62/62 - 00:02:03  
To activate this project's virtualenv, run pipenv shell.  
Alternatively, run a command inside the virtualenv with pipenv run.  
(base) PS D:\lambdaschool\ds-unit-2-sprint-4-project> pipenv shell  
Launching subshell in virtual environment…  
Windows PowerShell  
Copyright (C) Microsoft Corporation. All rights reserved.  

PS D:\lambdaschool\ds-unit-2-sprint-4-project> python run.py  
Running on http://127.0.0.1:8050/  
Debugger PIN: 079-739-012  
 * Serving Flask app "app" (lazy loading)  
 * Environment: production  
   WARNING: This is a development server. Do not use it in a production deployment.  
   Use a production WSGI server instead.  
 * Debug mode: on  
Running on http://127.0.0.1:8050/  
Debugger PIN: 685-819-428  
```
