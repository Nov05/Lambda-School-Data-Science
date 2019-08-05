2019-08-05   
Windows 10, Anaconda3  

## Anaconda3 Powershell Prompt

```
(base) PS C:\Users\*> cd d:/lambdaschool
(base) PS D:\lambdaschool> ls


    Directory: D:\lambdaschool


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----       2019-08-05  09:48 AM                DS-Unit-2-Sprint-4-Project
d-----       2019-08-05  06:15 PM                lambdata-nov05


(base) PS D:\lambdaschool> cd lambdata-nov05
(base) PS D:\lambdaschool\lambdata-nov05> conda activate ds-unit3
(ds-unit3) PS D:\lambdaschool\lambdata-nov05> conda env export > environment.yml
(ds-unit3) PS D:\lambdaschool\lambdata-nov05> ls


    Directory: D:\lambdaschool\lambdata-nov05


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----       2019-08-05  06:26 PM           2356 environment.yml
-a----       2019-08-05  06:15 PM             93 README.md


(ds-unit3) PS D:\lambdaschool\lambdata-nov05> cat environment.yml
name: ds-unit3
channels:
  - defaults
dependencies:
  - blas=1.0=mkl
  - ca-certificates=2019.5.15=0
  - certifi=2019.6.16=py37_1
  - cycler=0.10.0=py37_0
  - freetype=2.9.1=ha9979f8_1
  - icc_rt=2019.0.0=h0cc432a_1
  - icu=58.2=ha66f8fd_1
  - intel-openmp=2019.4=245
  - jpeg=9b=hb83a4c4_2
  - kiwisolver=1.1.0=py37ha925a31_0
  - libpng=1.6.37=h2a8f88b_0
  - matplotlib=3.1.0=py37hc8f65d3_0
  - mkl=2019.4=245
  - mkl_fft=1.0.12=py37h14836fe_0
  - mkl_random=1.0.2=py37h343c172_0
  - numpy=1.16.4=py37h19fb1c0_0
  - numpy-base=1.16.4=py37hc3f5095_0
  - openssl=1.1.1c=he774522_1
  - pandas=0.25.0=py37ha925a31_0
  - pip=19.1.1=py37_0
  - pyparsing=2.4.0=py_0
  - pyqt=5.9.2=py37h6538335_2
  - python=3.7.3=h8c8aaf0_1
  - python-dateutil=2.8.0=py37_0
  - pytz=2019.1=py_0
  - qt=5.9.7=vc14h73c81de_0
  - setuptools=41.0.1=py37_0
  - sip=4.19.8=py37h6538335_0
  - six=1.12.0=py37_0
  - sqlite=3.29.0=he774522_0
  - tornado=6.0.3=py37he774522_0
  - vc=14.1=h0510ff6_4
  - vs2015_runtime=14.15.26706=h3a45250_4
  - wheel=0.33.4=py37_0
  - wincertstore=0.2=py37_0
  - zlib=1.2.11=h62dcd97_3
prefix: C:\Users\*\Anaconda3\envs\ds-unit3
```

* recreate the environment by `conda env create -f environment.yml`  
https://medium.com/@krishnaregmi/pipenv-vs-virtualenv-vs-conda-environment-3dde3f6869ed  

## install jupyter notebook

```
(ds-unit3) PS D:\lambdaschool\lambdata-nov05> conda install jupyter
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\Users\*\Anaconda3\envs\ds-unit3

  added / updated specs:
    - jupyter


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    ipython-7.7.0              |   py37h39e3cac_0         1.1 MB
    qtconsole-4.5.2            |             py_0          92 KB
    ------------------------------------------------------------
                                           Total:         1.2 MB

The following NEW packages will be INSTALLED:

  attrs              pkgs/main/win-64::attrs-19.1.0-py37_1
  backcall           pkgs/main/win-64::backcall-0.1.0-py37_0
  bleach             pkgs/main/win-64::bleach-3.1.0-py37_0
  colorama           pkgs/main/win-64::colorama-0.4.1-py37_0
  decorator          pkgs/main/win-64::decorator-4.4.0-py37_1
  defusedxml         pkgs/main/noarch::defusedxml-0.6.0-py_0
  entrypoints        pkgs/main/win-64::entrypoints-0.3-py37_0
  ipykernel          pkgs/main/win-64::ipykernel-5.1.1-py37h39e3cac_0
  ipython            pkgs/main/win-64::ipython-7.7.0-py37h39e3cac_0
  ipython_genutils   pkgs/main/win-64::ipython_genutils-0.2.0-py37_0
  ipywidgets         pkgs/main/noarch::ipywidgets-7.5.0-py_0
  jedi               pkgs/main/win-64::jedi-0.13.3-py37_0
  jinja2             pkgs/main/win-64::jinja2-2.10.1-py37_0
  jsonschema         pkgs/main/win-64::jsonschema-3.0.1-py37_0
  jupyter            pkgs/main/win-64::jupyter-1.0.0-py37_7
  jupyter_client     pkgs/main/noarch::jupyter_client-5.3.1-py_0
  jupyter_console    pkgs/main/win-64::jupyter_console-6.0.0-py37_0
  jupyter_core       pkgs/main/noarch::jupyter_core-4.5.0-py_0
  libsodium          pkgs/main/win-64::libsodium-1.0.16-h9d3ae62_0
  m2w64-gcc-libgfor~ pkgs/msys2/win-64::m2w64-gcc-libgfortran-5.3.0-6
  m2w64-gcc-libs     pkgs/msys2/win-64::m2w64-gcc-libs-5.3.0-7
  m2w64-gcc-libs-co~ pkgs/msys2/win-64::m2w64-gcc-libs-core-5.3.0-7
  m2w64-gmp          pkgs/msys2/win-64::m2w64-gmp-6.1.0-2
  m2w64-libwinpthre~ pkgs/msys2/win-64::m2w64-libwinpthread-git-5.0.0.4634.697f757-2
  markupsafe         pkgs/main/win-64::markupsafe-1.1.1-py37he774522_0
  mistune            pkgs/main/win-64::mistune-0.8.4-py37he774522_0
  msys2-conda-epoch  pkgs/msys2/win-64::msys2-conda-epoch-20160418-1
  nbconvert          pkgs/main/noarch::nbconvert-5.5.0-py_0
  nbformat           pkgs/main/win-64::nbformat-4.4.0-py37_0
  notebook           pkgs/main/win-64::notebook-6.0.0-py37_0
  pandoc             pkgs/main/win-64::pandoc-2.2.3.2-0
  pandocfilters      pkgs/main/win-64::pandocfilters-1.4.2-py37_1
  parso              pkgs/main/noarch::parso-0.5.0-py_0
  pickleshare        pkgs/main/win-64::pickleshare-0.7.5-py37_0
  prometheus_client  pkgs/main/noarch::prometheus_client-0.7.1-py_0
  prompt_toolkit     pkgs/main/win-64::prompt_toolkit-2.0.9-py37_0
  pygments           pkgs/main/noarch::pygments-2.4.2-py_0
  pyrsistent         pkgs/main/win-64::pyrsistent-0.14.11-py37he774522_0
  pywinpty           pkgs/main/win-64::pywinpty-0.5.5-py37_1000
  pyzmq              pkgs/main/win-64::pyzmq-18.0.0-py37ha925a31_0
  qtconsole          pkgs/main/noarch::qtconsole-4.5.2-py_0
  send2trash         pkgs/main/win-64::send2trash-1.5.0-py37_0
  terminado          pkgs/main/win-64::terminado-0.8.2-py37_0
  testpath           pkgs/main/win-64::testpath-0.4.2-py37_0
  traitlets          pkgs/main/win-64::traitlets-4.3.2-py37_0
  wcwidth            pkgs/main/win-64::wcwidth-0.1.7-py37_0
  webencodings       pkgs/main/win-64::webencodings-0.5.1-py37_1
  widgetsnbextension pkgs/main/win-64::widgetsnbextension-3.5.0-py37_0
  winpty             pkgs/main/win-64::winpty-0.4.3-4
  zeromq             pkgs/main/win-64::zeromq-4.3.1-h33f27b4_3


Proceed ([y]/n)? y


Downloading and Extracting Packages
qtconsole-4.5.2      | 92 KB     | ############################################################################ | 100%
ipython-7.7.0        | 1.1 MB    | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: / DEBUG menuinst_win32:__init__(199): Menu: name: 'Anaconda${PY_VER} ${PLATFORM}', prefix: 'C:\Users\*\Anaconda3\envs\ds-unit3', env_name: 'ds-unit3', mode: 'user', used_mode: 'user'
DEBUG menuinst_win32:create(323): Shortcut cmd is C:\Users\*\Anaconda3\python.exe, args are ['C:\\Users\\*\\Anaconda3\\cwp.py', 'C:\\Users\\*\\Anaconda3\\envs\\ds-unit3', 'C:\\Users\\*\\Anaconda3\\envs\\ds-unit3\\python.exe', 'C:\\Users\\*\\Anaconda3\\envs\\ds-unit3\\Scripts\\jupyter-notebook-script.py', '"%USERPROFILE%/"']
done
(ds-unit3) PS D:\lambdaschool\lambdata-nov05> jupyter notebook
[I 18:42:28.567 NotebookApp] Serving notebooks from local directory: D:\lambdaschool\lambdata-nov05
[I 18:42:28.567 NotebookApp] The Jupyter Notebook is running at:
[I 18:42:28.570 NotebookApp] http://localhost:8888/?token=a29cb6b66bae8e172ae67cedde2d3b1d43490574d3a3ee21
[I 18:42:28.578 NotebookApp]  or http://127.0.0.1:8888/?token=a29cb6b66bae8e172ae67cedde2d3b1d43490574d3a3ee21
[I 18:42:28.581 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 18:42:28.663 NotebookApp]

    To access the notebook, open this file in a browser:
        file:///C:/Users/*/AppData/Roaming/jupyter/runtime/nbserver-15468-open.html
    Or copy and paste one of these URLs:
        http://localhost:8888/?token=a29cb6b66bae8e172ae67cedde2d3b1d43490574d3a3ee21
     or http://127.0.0.1:8888/?token=a29cb6b66bae8e172ae67cedde2d3b1d43490574d3a3ee21
[E 18:42:38.483 NotebookApp] Could not open static file ''
[W 18:42:38.854 NotebookApp] 404 GET /static/components/react/react-dom.production.min.js (::1) 36.90ms referer=http://localhost:8888/tree?token=a29cb6b66bae8e172ae67cedde2d3b1d43490574d3a3ee21
[W 18:42:38.891 NotebookApp] 404 GET /static/components/react/react-dom.production.min.js (::1) 2.99ms referer=http://localhost:8888/tree?token=a29cb6b66bae8e172ae67cedde2d3b1d43490574d3a3ee21
```

