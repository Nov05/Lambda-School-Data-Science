2019-08-05  

Distribute Python packages with "setuptools" library  
https://packaging.python.org/tutorials/packaging-projects/  

Check the package at TestPyPI   
https://test.pypi.org/project/lambdata-nov05/  

GitHub repo  
https://github.com/Nov05/python-packages

**Note:** 
1. name in `__init__.py` or `setup.py` doesn't mind `-` or `_`, only "package folder name" would matter here (because folder name will be used as library name, if you name the folder "lambdata-nov05" then `import lambdata-nov05`, Python `import` can't read `-`, if you `import lambdata_nov05`, Python will throw **ModuleNotFoundError: No module named 'lambdata_nov05'**).  
2. name in `setup.py` is called "package distribution name". name in `__init__.py` is merely an attribute of the package object, so technically it can be anything (as long as python allows it), but it is better to keep the two same.  
3. remember to **update version number** in `setup.py` every time before you generate/upload distribution files.

<img src="https://github.com/Nov05/pictures/blob/master/pic001/2019-08-05%2021_03_19-Home.png?raw=true" width="400"><img src="https://github.com/Nov05/pictures/blob/master/pic001/2019-08-05%2022_05_14-2019-08-05%20create%20your%20own%20python%20package.ipynb%20-%20Colaboratory.png?raw=true" width="400">  

## Windowns 10, Anaconda3 Powershell Prompt

Make sure you have the latest versions of setuptools and wheel installed:
```
(base) PS D:\lambdaschool\python-packages> conda activate ds-unit3
(ds-unit3) PS D:\lambdaschool\python-packages> pip install --user --upgrade setuptools wheel
Requirement already up-to-date: setuptools in c:\users\*\anaconda3\envs\ds-unit3\lib\site-packages (41.0.1)
Requirement already up-to-date: wheel in c:\users\*\anaconda3\envs\ds-unit3\lib\site-packages (0.33.4)
(ds-unit3) PS D:\lambdaschool\python-packages>
```

Now run this command from the same directory where setup.py is located:
```
(ds-unit3) PS D:\lambdaschool\python-packages> python setup.py sdist bdist_wheel
running sdist
running egg_info
creating lambdata_nov05.egg-info
writing lambdata_nov05.egg-info\PKG-INFO
writing dependency_links to lambdata_nov05.egg-info\dependency_links.txt
writing top-level names to lambdata_nov05.egg-info\top_level.txt
writing manifest file 'lambdata_nov05.egg-info\SOURCES.txt'
reading manifest file 'lambdata_nov05.egg-info\SOURCES.txt'
writing manifest file 'lambdata_nov05.egg-info\SOURCES.txt'
running check
creating lambdata-nov05-0.0.1
creating lambdata-nov05-0.0.1\lambdata_nov05
creating lambdata-nov05-0.0.1\lambdata_nov05.egg-info
copying files to lambdata-nov05-0.0.1...
copying README.md -> lambdata-nov05-0.0.1
copying setup.py -> lambdata-nov05-0.0.1
copying lambdata_nov05\__init__.py -> lambdata-nov05-0.0.1\lambdata_nov05
copying lambdata_nov05.egg-info\PKG-INFO -> lambdata-nov05-0.0.1\lambdata_nov05.egg-info
copying lambdata_nov05.egg-info\SOURCES.txt -> lambdata-nov05-0.0.1\lambdata_nov05.egg-info
copying lambdata_nov05.egg-info\dependency_links.txt -> lambdata-nov05-0.0.1\lambdata_nov05.egg-info
copying lambdata_nov05.egg-info\top_level.txt -> lambdata-nov05-0.0.1\lambdata_nov05.egg-info
Writing lambdata-nov05-0.0.1\setup.cfg
creating dist
Creating tar archive
removing 'lambdata-nov05-0.0.1' (and everything under it)
running bdist_wheel
running build
running build_py
creating build
creating build\lib
creating build\lib\lambdata_nov05
copying lambdata_nov05\__init__.py -> build\lib\lambdata_nov05
installing to build\bdist.win-amd64\wheel
running install
running install_lib
creating build\bdist.win-amd64
creating build\bdist.win-amd64\wheel
creating build\bdist.win-amd64\wheel\lambdata_nov05
copying build\lib\lambdata_nov05\__init__.py -> build\bdist.win-amd64\wheel\.\lambdata_nov05
running install_egg_info
Copying lambdata_nov05.egg-info to build\bdist.win-amd64\wheel\.\lambdata_nov05-0.0.1-py3.7.egg-info
running install_scripts
adding license file "LICENSE" (matched pattern "LICEN[CS]E*")
creating build\bdist.win-amd64\wheel\lambdata_nov05-0.0.1.dist-info\WHEEL
creating 'dist\lambdata_nov05-0.0.1-py3-none-any.whl' and adding 'build\bdist.win-amd64\wheel' to it
adding 'lambdata_nov05/__init__.py'
adding 'lambdata_nov05-0.0.1.dist-info/LICENSE'
adding 'lambdata_nov05-0.0.1.dist-info/METADATA'
adding 'lambdata_nov05-0.0.1.dist-info/WHEEL'
adding 'lambdata_nov05-0.0.1.dist-info/top_level.txt'
adding 'lambdata_nov05-0.0.1.dist-info/RECORD'
removing build\bdist.win-amd64\wheel
```

... Now that you are registered, you can use twine to upload the distribution packages. You’ll need to install Twine:

```
(ds-unit3) PS D:\lambdaschool\python-packages> pip install --user --upgrade twine
Collecting twine
  Downloading https://files.pythonhosted.org/packages/28/90/59eec88c0b2ac9e47fe135959007acb93a3cc9f7146366e11fecf718dd15/twine-1.13.0-py2.py3-none-any.whl
Collecting requests-toolbelt!=0.9.0,>=0.8.0 (from twine)
  Downloading https://files.pythonhosted.org/packages/60/ef/7681134338fc097acef8d9b2f8abe0458e4d87559c689a8c306d0957ece5/requests_toolbelt-0.9.1-py2.py3-none-any.whl (54kB)
     |████████████████████████████████| 61kB 2.0MB/s
Collecting readme-renderer>=21.0 (from twine)
  Downloading https://files.pythonhosted.org/packages/c3/7e/d1aae793900f36b097cbfcc5e70eef82b5b56423a6c52a36dce51fedd8f0/readme_renderer-24.0-py2.py3-none-any.whl
Collecting requests!=2.15,!=2.16,>=2.5.0 (from twine)
  Downloading https://files.pythonhosted.org/packages/51/bd/23c926cd341ea6b7dd0b2a00aba99ae0f828be89d72b2190f27c11d4b7fb/requests-2.22.0-py2.py3-none-any.whl (57kB)
     |████████████████████████████████| 61kB 1.9MB/s
Collecting pkginfo>=1.4.2 (from twine)
  Downloading https://files.pythonhosted.org/packages/e6/d5/451b913307b478c49eb29084916639dc53a88489b993530fed0a66bab8b9/pkginfo-1.5.0.1-py2.py3-none-any.whl
Requirement already satisfied, skipping upgrade: setuptools>=0.7.0 in c:\users\*\anaconda3\envs\ds-unit3\lib\site-packages (from twine) (41.0.1)
Collecting tqdm>=4.14 (from twine)
  Downloading https://files.pythonhosted.org/packages/9f/3d/7a6b68b631d2ab54975f3a4863f3c4e9b26445353264ef01f465dc9b0208/tqdm-4.32.2-py2.py3-none-any.whl (50kB)
     |████████████████████████████████| 51kB 3.2MB/s
Requirement already satisfied, skipping upgrade: six in c:\users\*\anaconda3\envs\ds-unit3\lib\site-packages (from readme-renderer>=21.0->twine) (1.12.0)
Requirement already satisfied, skipping upgrade: Pygments in c:\users\*\anaconda3\envs\ds-unit3\lib\site-packages (from readme-renderer>=21.0->twine) (2.4.2)
Requirement already satisfied, skipping upgrade: bleach>=2.1.0 in c:\users\*\anaconda3\envs\ds-unit3\lib\site-packages (from readme-renderer>=21.0->twine) (3.1.0)
Collecting docutils>=0.13.1 (from readme-renderer>=21.0->twine)
  Downloading https://files.pythonhosted.org/packages/22/cd/a6aa959dca619918ccb55023b4cb151949c64d4d5d55b3f4ffd7eee0c6e8/docutils-0.15.2-py3-none-any.whl (547kB)
     |████████████████████████████████| 552kB 2.2MB/s
Requirement already satisfied, skipping upgrade: certifi>=2017.4.17 in c:\users\*\anaconda3\envs\ds-unit3\lib\site-packages (from requests!=2.15,!=2.16,>=2.5.0->twine) (2019.6.16)
Collecting idna<2.9,>=2.5 (from requests!=2.15,!=2.16,>=2.5.0->twine)
  Downloading https://files.pythonhosted.org/packages/14/2c/cd551d81dbe15200be1cf41cd03869a46fe7226e7450af7a6545bfc474c9/idna-2.8-py2.py3-none-any.whl (58kB)
     |████████████████████████████████| 61kB 3.8MB/s
Collecting chardet<3.1.0,>=3.0.2 (from requests!=2.15,!=2.16,>=2.5.0->twine)
  Downloading https://files.pythonhosted.org/packages/bc/a9/01ffebfb562e4274b6487b4bb1ddec7ca55ec7510b22e4c51f14098443b8/chardet-3.0.4-py2.py3-none-any.whl (133kB)
     |████████████████████████████████| 143kB 3.2MB/s
Collecting urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 (from requests!=2.15,!=2.16,>=2.5.0->twine)
  Downloading https://files.pythonhosted.org/packages/e6/60/247f23a7121ae632d62811ba7f273d0e58972d75e58a94d329d51550a47d/urllib3-1.25.3-py2.py3-none-any.whl (150kB)
     |████████████████████████████████| 153kB 3.3MB/s
Requirement already satisfied, skipping upgrade: webencodings in c:\users\*\anaconda3\envs\ds-unit3\lib\site-packages (from bleach>=2.1.0->readme-renderer>=21.0->twine) (0.5.1)
Installing collected packages: idna, chardet, urllib3, requests, requests-toolbelt, docutils, readme-renderer, pkginfo, tqdm, twine
  WARNING: The script chardetect.exe is installed in 'C:\Users\*\AppData\Roaming\Python\Python37\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
  WARNING: The script pkginfo.exe is installed in 'C:\Users\*\AppData\Roaming\Python\Python37\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
  WARNING: The script tqdm.exe is installed in 'C:\Users\*\AppData\Roaming\Python\Python37\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
  WARNING: The script twine.exe is installed in 'C:\Users\*\AppData\Roaming\Python\Python37\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed chardet-3.0.4 docutils-0.15.2 idna-2.8 pkginfo-1.5.0.1 readme-renderer-24.0 requests-2.22.0 requests-toolbelt-0.9.1 tqdm-4.32.2 twine-1.13.0 urllib3-1.25.3
```

Once installed, run Twine to upload all of the archives under dist:
```
(ds-unit3) PS D:\lambdaschool\python-packages> python -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*
Enter your username: nov05
Enter your password:
Uploading distributions to https://test.pypi.org/legacy/
Uploading lambdata_nov05-0.0.1-py3-none-any.whl
100%|█████████████████████████████████████████████████████████████████████████████| 5.39k/5.39k [00:00<00:00, 26.3kB/s]
Uploading lambdata-nov05-0.0.1.tar.gz
100%|█████████████████████████████████████████████████████████████████████████████| 4.17k/4.17k [00:01<00:00, 3.64kB/s]
```

Now you should be able to check the package at TestPyPI.  

<img src="https://github.com/Nov05/pictures/blob/master/pic001/2019-08-05%2021_06_04-TestPyPI.png?raw=true">
