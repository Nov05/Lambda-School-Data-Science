2019-08-23   
Google Colab   

# !sudo apt purge python2.7-minimal
remove python 2.7
```
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libaio1 libboost-atomic-dev libboost-atomic1.65-dev libboost-atomic1.65.1
  libboost-chrono-dev libboost-chrono1.65-dev libboost-chrono1.65.1
  libboost-container-dev libboost-container1.65-dev libboost-container1.65.1
  libboost-context-dev libboost-context1.65-dev libboost-context1.65.1
  libboost-coroutine-dev libboost-coroutine1.65-dev libboost-coroutine1.65.1
  libboost-date-time-dev libboost-date-time1.65-dev libboost-date-time1.65.1
  libboost-dev libboost-exception-dev libboost-exception1.65-dev
  libboost-fiber-dev libboost-fiber1.65-dev libboost-fiber1.65.1
  libboost-filesystem-dev libboost-filesystem1.65-dev
  libboost-filesystem1.65.1 libboost-graph-dev libboost-graph-parallel-dev
  libboost-graph-parallel1.65-dev libboost-graph-parallel1.65.1
  libboost-graph1.65-dev libboost-graph1.65.1 libboost-iostreams-dev
  libboost-iostreams1.65-dev libboost-iostreams1.65.1 libboost-locale-dev
  libboost-locale1.65-dev libboost-locale1.65.1 libboost-log-dev
  libboost-log1.65-dev libboost-log1.65.1 libboost-math-dev
  libboost-math1.65-dev libboost-math1.65.1 libboost-mpi-dev
  libboost-mpi1.65-dev libboost-mpi1.65.1 libboost-numpy-dev
  libboost-numpy1.65-dev libboost-numpy1.65.1 libboost-program-options-dev
  libboost-program-options1.65-dev libboost-program-options1.65.1
  libboost-python1.65.1 libboost-random-dev libboost-random1.65-dev
  libboost-random1.65.1 libboost-regex-dev libboost-regex1.65-dev
  libboost-regex1.65.1 libboost-serialization-dev
  libboost-serialization1.65-dev libboost-serialization1.65.1
  libboost-signals-dev libboost-signals1.65-dev libboost-signals1.65.1
  libboost-stacktrace-dev libboost-stacktrace1.65-dev
  libboost-stacktrace1.65.1 libboost-system-dev libboost-system1.65-dev
  libboost-system1.65.1 libboost-test-dev libboost-test1.65-dev
  libboost-test1.65.1 libboost-thread-dev libboost-thread1.65-dev
  libboost-thread1.65.1 libboost-timer-dev libboost-timer1.65-dev
  libboost-timer1.65.1 libboost-tools-dev libboost-type-erasure-dev
  libboost-type-erasure1.65-dev libboost-type-erasure1.65.1 libboost-wave-dev
  libboost-wave1.65-dev libboost-wave1.65.1 libboost1.65-dev
  libboost1.65-tools-dev libpython-stdlib librados2 librbd1 mpi-default-bin
  mpi-default-dev
Use 'sudo apt autoremove' to remove them.
The following packages will be REMOVED:
  fio* libboost-all-dev* libboost-mpi-python-dev* libboost-mpi-python1.65-dev*
  libboost-mpi-python1.65.1* libboost-python-dev* libboost-python1.65-dev*
  python* python-dev* python-gdal* python-minimal* python-numpy* python-tk*
  python2.7* python2.7-dev* python2.7-minimal*
0 upgraded, 0 newly installed, 16 to remove and 14 not upgraded.
After this operation, 24.2 MB disk space will be freed.
(Reading database ... 131183 files and directories currently installed.)
Removing fio (3.1-1) ...
Removing libboost-all-dev (1.65.1.0ubuntu1) ...
Removing libboost-mpi-python-dev (1.65.1.0ubuntu1) ...
Removing libboost-mpi-python1.65-dev (1.65.1+dfsg-0ubuntu5) ...
Removing libboost-mpi-python1.65.1 (1.65.1+dfsg-0ubuntu5) ...
Removing libboost-python-dev (1.65.1.0ubuntu1) ...
Removing libboost-python1.65-dev (1.65.1+dfsg-0ubuntu5) ...
Removing python-tk (2.7.16-2~18.04) ...
Removing python-gdal (2.2.3+dfsg-2) ...
Removing python-numpy (1:1.13.3-2ubuntu1) ...
Removing python-dev (2.7.15~rc1-1) ...
Removing python2.7-dev (2.7.15-4ubuntu4~18.04) ...
Removing python (2.7.15~rc1-1) ...
Removing python-minimal (2.7.15~rc1-1) ...
Removing python2.7 (2.7.15-4ubuntu4~18.04) ...
Removing python2.7-minimal (2.7.15-4ubuntu4~18.04) ...
Unlinking and removing bytecode for runtime python2.7
Processing triggers for mime-support (3.60ubuntu1) ...
Processing triggers for libc-bin (2.27-3ubuntu1) ...
Processing triggers for man-db (2.8.3-2ubuntu0.1) ...
(Reading database ... 130434 files and directories currently installed.)
Purging configuration files for python (2.7.15~rc1-1) ...
Purging configuration files for python2.7-minimal (2.7.15-4ubuntu4~18.04) ...
```

# !jupyter notebook
Why is Python 2.7 called here?
```
/usr/local/lib/python2.7/dist-packages/IPython/utils/traitlets.py:5: UserWarning: IPython.utils.traitlets has moved to a top-level traitlets package.
  warn("IPython.utils.traitlets has moved to a top-level traitlets package.")
Traceback (most recent call last):
  File "/usr/local/bin/jupyter-notebook", line 10, in <module>
    sys.exit(main())
  File "/usr/local/lib/python2.7/dist-packages/jupyter_core/application.py", line 267, in launch_instance
    return super(JupyterApp, cls).launch_instance(argv=argv, **kwargs)
  File "/usr/local/lib/python2.7/dist-packages/traitlets/config/application.py", line 657, in launch_instance
    app.initialize(argv)
  File "</usr/local/lib/python2.7/dist-packages/decorator.pyc:decorator-gen-7>", line 2, in initialize
  File "/usr/local/lib/python2.7/dist-packages/traitlets/config/application.py", line 87, in catch_config_error
    return method(app, *args, **kwargs)
  File "/usr/local/lib/python2.7/dist-packages/notebook/notebookapp.py", line 1368, in initialize
    self.init_webapp()
  File "/usr/local/lib/python2.7/dist-packages/notebook/notebookapp.py", line 1188, in init_webapp
    self.http_server.listen(port, self.ip)
  File "/usr/local/lib/python2.7/dist-packages/tornado/tcpserver.py", line 142, in listen
    sockets = bind_sockets(port, address=address)
  File "/usr/local/lib/python2.7/dist-packages/tornado/netutil.py", line 197, in bind_sockets
    sock.bind(sockaddr)
  File "/usr/lib/python2.7/socket.py", line 228, in meth
    return getattr(self._sock,name)(*args)
socket.error: [Errno 99] Cannot assign requested address
```

# !FLASK_APP=iris.py flask run  
Why is Python 2.7 called here too?  
```
* Serving Flask app "iris.py"
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: off
Traceback (most recent call last):
  File "/usr/local/bin/flask", line 10, in <module>
    sys.exit(main())
  File "/usr/local/lib/python2.7/dist-packages/flask/cli.py", line 966, in main
    cli.main(prog_name="python -m flask" if as_module else None)
  File "/usr/local/lib/python2.7/dist-packages/flask/cli.py", line 586, in main
    return super(FlaskGroup, self).main(*args, **kwargs)
  File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 717, in main
    rv = self.invoke(ctx)
  File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 1137, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
  File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 956, in invoke
    return ctx.invoke(self.callback, **ctx.params)
  File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 555, in invoke
    return callback(*args, **kwargs)
  File "/usr/local/lib/python2.7/dist-packages/click/decorators.py", line 64, in new_func
    return ctx.invoke(f, obj, *args, **kwargs)
  File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 555, in invoke
    return callback(*args, **kwargs)
  File "/usr/local/lib/python2.7/dist-packages/flask/cli.py", line 848, in run_command
    app = DispatchingApp(info.load_app, use_eager_loading=eager_loading)
  File "/usr/local/lib/python2.7/dist-packages/flask/cli.py", line 305, in __init__
    self._load_unlocked()
  File "/usr/local/lib/python2.7/dist-packages/flask/cli.py", line 330, in _load_unlocked
    self._app = rv = self.loader()
  File "/usr/local/lib/python2.7/dist-packages/flask/cli.py", line 388, in load_app
    app = locate_app(self, import_name, name)
  File "/usr/local/lib/python2.7/dist-packages/flask/cli.py", line 240, in locate_app
    __import__(module_name)
  File "/content/iris.py", line 6, in <module>
    model_iris = pickle.load(open('model.pkl', 'rb'))
  File "/usr/lib/python2.7/pickle.py", line 1384, in load
    return Unpickler(file).load()
  File "/usr/lib/python2.7/pickle.py", line 864, in load
    dispatch[key](self)
  File "/usr/lib/python2.7/pickle.py", line 892, in load_proto
    raise ValueError, "unsupported pickle protocol: %d" % proto
ValueError: unsupported pickle protocol: 3
```

# !pip install jupyter notebook
```
Requirement already satisfied: jupyter in /usr/local/lib/python3.6/dist-packages (1.0.0)
Requirement already satisfied: notebook in /usr/local/lib/python3.6/dist-packages (5.2.2)
Requirement already satisfied: ipywidgets in /usr/local/lib/python3.6/dist-packages (from jupyter) (7.5.1)
Requirement already satisfied: ipykernel in /usr/local/lib/python3.6/dist-packages (from jupyter) (4.6.1)
Requirement already satisfied: nbconvert in /usr/local/lib/python3.6/dist-packages (from jupyter) (5.6.0)
Requirement already satisfied: qtconsole in /usr/local/lib/python3.6/dist-packages (from jupyter) (4.5.4)
Requirement already satisfied: jupyter-console in /usr/local/lib/python3.6/dist-packages (from jupyter) (5.2.0)
Requirement already satisfied: jupyter-client in /usr/local/lib/python3.6/dist-packages (from notebook) (5.3.1)
Requirement already satisfied: jupyter-core in /usr/local/lib/python3.6/dist-packages (from notebook) (4.5.0)
Requirement already satisfied: tornado>=4 in /usr/local/lib/python3.6/dist-packages (from notebook) (4.5.3)
Requirement already satisfied: terminado>=0.3.3; sys_platform != "win32" in /usr/local/lib/python3.6/dist-packages (from notebook) (0.8.2)
Requirement already satisfied: nbformat in /usr/local/lib/python3.6/dist-packages (from notebook) (4.4.0)
Requirement already satisfied: traitlets>=4.2.1 in /usr/local/lib/python3.6/dist-packages (from notebook) (4.3.2)
Requirement already satisfied: jinja2 in /usr/local/lib/python3.6/dist-packages (from notebook) (2.10.1)
Requirement already satisfied: ipython-genutils in /usr/local/lib/python3.6/dist-packages (from notebook) (0.2.0)
Requirement already satisfied: widgetsnbextension~=3.5.0 in /usr/local/lib/python3.6/dist-packages (from ipywidgets->jupyter) (3.5.1)
Requirement already satisfied: ipython>=4.0.0; python_version >= "3.3" in /usr/local/lib/python3.6/dist-packages (from ipywidgets->jupyter) (5.5.0)
Requirement already satisfied: pygments in /usr/local/lib/python3.6/dist-packages (from nbconvert->jupyter) (2.1.3)
Requirement already satisfied: testpath in /usr/local/lib/python3.6/dist-packages (from nbconvert->jupyter) (0.4.2)
Requirement already satisfied: mistune<2,>=0.8.1 in /usr/local/lib/python3.6/dist-packages (from nbconvert->jupyter) (0.8.4)
Requirement already satisfied: entrypoints>=0.2.2 in /usr/local/lib/python3.6/dist-packages (from nbconvert->jupyter) (0.3)
Requirement already satisfied: pandocfilters>=1.4.1 in /usr/local/lib/python3.6/dist-packages (from nbconvert->jupyter) (1.4.2)
Requirement already satisfied: defusedxml in /usr/local/lib/python3.6/dist-packages (from nbconvert->jupyter) (0.6.0)
Requirement already satisfied: bleach in /usr/local/lib/python3.6/dist-packages (from nbconvert->jupyter) (3.1.0)
Requirement already satisfied: prompt-toolkit<2.0.0,>=1.0.0 in /usr/local/lib/python3.6/dist-packages (from jupyter-console->jupyter) (1.0.16)
Requirement already satisfied: pyzmq>=13 in /usr/local/lib/python3.6/dist-packages (from jupyter-client->notebook) (17.0.0)
Requirement already satisfied: python-dateutil>=2.1 in /usr/local/lib/python3.6/dist-packages (from jupyter-client->notebook) (2.5.3)
Requirement already satisfied: ptyprocess; os_name != "nt" in /usr/local/lib/python3.6/dist-packages (from terminado>=0.3.3; sys_platform != "win32"->notebook) (0.6.0)
Requirement already satisfied: jsonschema!=2.5.0,>=2.4 in /usr/local/lib/python3.6/dist-packages (from nbformat->notebook) (2.6.0)
Requirement already satisfied: six in /usr/local/lib/python3.6/dist-packages (from traitlets>=4.2.1->notebook) (1.12.0)
Requirement already satisfied: decorator in /usr/local/lib/python3.6/dist-packages (from traitlets>=4.2.1->notebook) (4.4.0)
Requirement already satisfied: MarkupSafe>=0.23 in /usr/local/lib/python3.6/dist-packages (from jinja2->notebook) (1.1.1)
Requirement already satisfied: pickleshare in /usr/local/lib/python3.6/dist-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets->jupyter) (0.7.5)
Requirement already satisfied: pexpect; sys_platform != "win32" in /usr/local/lib/python3.6/dist-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets->jupyter) (4.7.0)
Requirement already satisfied: simplegeneric>0.8 in /usr/local/lib/python3.6/dist-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets->jupyter) (0.8.1)
Requirement already satisfied: setuptools>=18.5 in /usr/local/lib/python3.6/dist-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets->jupyter) (41.2.0)
Requirement already satisfied: webencodings in /usr/local/lib/python3.6/dist-packages (from bleach->nbconvert->jupyter) (0.5.1)
Requirement already satisfied: wcwidth in /usr/local/lib/python3.6/dist-packages (from prompt-toolkit<2.0.0,>=1.0.0->jupyter-console->jupyter) (0.1.7)
```

# !jupyter notebook --version  
!ipython --version  
!pip install ipython   
```
5.2.2
5.5.0
Requirement already satisfied: ipython in /usr/local/lib/python2.7/dist-packages (5.5.0)
Requirement already satisfied: simplegeneric>0.8 in /usr/local/lib/python2.7/dist-packages (from ipython) (0.8.1)
Requirement already satisfied: pickleshare in /usr/local/lib/python2.7/dist-packages (from ipython) (0.7.5)
Requirement already satisfied: backports.shutil-get-terminal-size; python_version == "2.7" in /usr/local/lib/python2.7/dist-packages (from ipython) (1.0.0)
Requirement already satisfied: pathlib2; python_version == "2.7" or python_version == "3.3" in /usr/local/lib/python2.7/dist-packages (from ipython) (2.3.4)
Requirement already satisfied: pexpect; sys_platform != "win32" in /usr/local/lib/python2.7/dist-packages (from ipython) (4.7.0)
Requirement already satisfied: traitlets>=4.2 in /usr/local/lib/python2.7/dist-packages (from ipython) (4.3.2)
Requirement already satisfied: pygments in /usr/local/lib/python2.7/dist-packages (from ipython) (2.1.3)
Requirement already satisfied: decorator in /usr/local/lib/python2.7/dist-packages (from ipython) (4.4.0)
Requirement already satisfied: prompt-toolkit<2.0.0,>=1.0.4 in /usr/local/lib/python2.7/dist-packages (from ipython) (1.0.16)
Requirement already satisfied: setuptools>=18.5 in /usr/local/lib/python2.7/dist-packages (from ipython) (41.2.0)
Requirement already satisfied: six in /usr/local/lib/python2.7/dist-packages (from pathlib2; python_version == "2.7" or python_version == "3.3"->ipython) (1.12.0)
Requirement already satisfied: scandir; python_version < "3.5" in /usr/local/lib/python2.7/dist-packages (from pathlib2; python_version == "2.7" or python_version == "3.3"->ipython) (1.10.0)
Requirement already satisfied: ptyprocess>=0.5 in /usr/local/lib/python2.7/dist-packages (from pexpect; sys_platform != "win32"->ipython) (0.6.0)
Requirement already satisfied: enum34; python_version == "2.7" in /usr/local/lib/python2.7/dist-packages (from traitlets>=4.2->ipython) (1.1.6)
Requirement already satisfied: ipython-genutils in /usr/local/lib/python2.7/dist-packages (from traitlets>=4.2->ipython) (0.2.0)
Requirement already satisfied: wcwidth in /usr/local/lib/python2.7/dist-packages (from prompt-toolkit<2.0.0,>=1.0.4->ipython) (0.1.7)
```



# !jupyter notebook --help
```
The Jupyter HTML Notebook.

This launches a Tornado based HTML Notebook Server that serves up an
HTML5/Javascript Notebook client.

Subcommands
-----------

Subcommands are launched as `jupyter-notebook cmd [args]`. For information on
using subcommand 'cmd', do: `jupyter-notebook cmd -h`.

stop
    Stop currently running notebook server for a given port
password
    Set a password for the notebook server.
list
    List currently running notebook servers.

Options
-------

Arguments that take values are actually convenience aliases to full
Configurables, whose aliases are listed on the help line. For more information
on full configurables, see '--help-all'.

--script
    DEPRECATED, IGNORED
--pylab
    DISABLED: use %pylab or %matplotlib in the notebook to enable matplotlib.
--debug
    set log level to logging.DEBUG (maximize logging output)
--no-browser
    Don't open the notebook in a browser after startup.
--allow-root
    Allow the notebook to be run from root user.
-y
    Answer yes to any questions instead of prompting.
--no-mathjax
    Disable MathJax
    
    MathJax is the javascript library Jupyter uses to render math/LaTeX. It is
    very large, so you may want to disable it if you have a slow internet
    connection, or for offline use of the notebook.
    
    When disabled, equations etc. will appear as their untransformed TeX source.
--no-script
    DEPRECATED, IGNORED
--generate-config
    generate default config file
--certfile=<Unicode> (NotebookApp.certfile)
    Default: u''
    The full path to an SSL/TLS certificate file.
--ip=<Unicode> (NotebookApp.ip)
    Default: 'localhost'
    The IP address the notebook server will listen on.
--pylab=<Unicode> (NotebookApp.pylab)
    Default: 'disabled'
    DISABLED: use %pylab or %matplotlib in the notebook to enable matplotlib.
--log-level=<Enum> (Application.log_level)
    Default: 30
    Choices: (0, 10, 20, 30, 40, 50, 'DEBUG', 'INFO', 'WARN', 'ERROR', 'CRITICAL')
    Set the log level by value or name.
--port-retries=<Integer> (NotebookApp.port_retries)
    Default: 50
    The number of additional ports to try if the specified port is not
    available.
--notebook-dir=<Unicode> (NotebookApp.notebook_dir)
    Default: u''
    The directory to use for notebooks and kernels.
--keyfile=<Unicode> (NotebookApp.keyfile)
    Default: u''
    The full path to a private key file for usage with SSL/TLS.
--client-ca=<Unicode> (NotebookApp.client_ca)
    Default: u''
    The full path to a certificate authority certificate for SSL/TLS client
    authentication.
--config=<Unicode> (JupyterApp.config_file)
    Default: u''
    Full path of a config file.
--port=<Integer> (NotebookApp.port)
    Default: 8888
    The port the notebook server will listen on.
--transport=<CaselessStrEnum> (KernelManager.transport)
    Default: 'tcp'
    Choices: [u'tcp', u'ipc']
--browser=<Unicode> (NotebookApp.browser)
    Default: u''
    Specify what command to use to invoke a web browser when opening the
    notebook. If not specified, the default browser will be determined by the
    `webbrowser` standard library module, which allows setting of the BROWSER
    environment variable to override it.

To see all available configurables, use `--help-all`

Examples
--------

    jupyter notebook                       # start the notebook
    jupyter notebook --certfile=mycert.pem # use SSL/TLS certificate
    jupyter notebook password              # enter a password to protect the server
```



# !python -m pip install --upgrade pip setuptools wheel  
!python3 -m pip install --upgrade pip setuptools wheel   
```
Requirement already up-to-date: pip in /usr/local/lib/python2.7/dist-packages (19.2.2)
Requirement already up-to-date: setuptools in /usr/local/lib/python2.7/dist-packages (41.2.0)
Requirement already up-to-date: wheel in /usr/local/lib/python2.7/dist-packages (0.33.6)
Requirement already up-to-date: pip in /usr/local/lib/python3.6/dist-packages (19.2.2)
Requirement already up-to-date: setuptools in /usr/local/lib/python3.6/dist-packages (41.2.0)
Requirement already up-to-date: wheel in /usr/local/lib/python3.6/dist-packages (0.33.6)
```



# !pip --version
!pip3 --version  
!pip3 install ipython   
```
pip 19.2.2 from /usr/local/lib/python2.7/dist-packages/pip (python 2.7)
pip 19.2.2 from /usr/local/lib/python3.6/dist-packages/pip (python 3.6)
Requirement already satisfied: ipython in /usr/local/lib/python3.6/dist-packages (5.5.0)
Requirement already satisfied: prompt-toolkit<2.0.0,>=1.0.4 in /usr/local/lib/python3.6/dist-packages (from ipython) (1.0.16)
Requirement already satisfied: setuptools>=18.5 in /usr/local/lib/python3.6/dist-packages (from ipython) (41.2.0)
Requirement already satisfied: decorator in /usr/local/lib/python3.6/dist-packages (from ipython) (4.4.0)
Requirement already satisfied: pexpect; sys_platform != "win32" in /usr/local/lib/python3.6/dist-packages (from ipython) (4.7.0)
Requirement already satisfied: traitlets>=4.2 in /usr/local/lib/python3.6/dist-packages (from ipython) (4.3.2)
Requirement already satisfied: pygments in /usr/local/lib/python3.6/dist-packages (from ipython) (2.1.3)
Requirement already satisfied: pickleshare in /usr/local/lib/python3.6/dist-packages (from ipython) (0.7.5)
Requirement already satisfied: simplegeneric>0.8 in /usr/local/lib/python3.6/dist-packages (from ipython) (0.8.1)
Requirement already satisfied: six>=1.9.0 in /usr/local/lib/python3.6/dist-packages (from prompt-toolkit<2.0.0,>=1.0.4->ipython) (1.12.0)
Requirement already satisfied: wcwidth in /usr/local/lib/python3.6/dist-packages (from prompt-toolkit<2.0.0,>=1.0.4->ipython) (0.1.7)
Requirement already satisfied: ptyprocess>=0.5 in /usr/local/lib/python3.6/dist-packages (from pexpect; sys_platform != "win32"->ipython) (0.6.0)
Requirement already satisfied: ipython-genutils in /usr/local/lib/python3.6/dist-packages (from traitlets>=4.2->ipython) (0.2.0)
```

# !pip3 install 'ipython==7.7.0'  
ERROR: jupyter-console 5.2.0 has requirement prompt-toolkit<2.0.0,>=1.0.0, but you'll have prompt-toolkit 2.0.9 which is incompatible.    
ERROR: google-colab 1.0.0 has requirement ipython~=5.5.0, but you'll have ipython 7.7.0 which is incompatible.    
```
Collecting ipython==7.7.0
  Downloading https://files.pythonhosted.org/packages/f6/c4/a79582814bdfe92bfca4d286a729304ffdf13f5135132cfcaea13cf1b2b3/ipython-7.7.0-py3-none-any.whl (774kB)
     |████████████████████████████████| 778kB 2.8MB/s 
Requirement already satisfied: decorator in /usr/local/lib/python3.6/dist-packages (from ipython==7.7.0) (4.4.0)
Collecting prompt-toolkit<2.1.0,>=2.0.0 (from ipython==7.7.0)
  Downloading https://files.pythonhosted.org/packages/f7/a7/9b1dd14ef45345f186ef69d175bdd2491c40ab1dfa4b2b3e4352df719ed7/prompt_toolkit-2.0.9-py3-none-any.whl (337kB)
     |████████████████████████████████| 337kB 49.2MB/s 
Requirement already satisfied: backcall in /usr/local/lib/python3.6/dist-packages (from ipython==7.7.0) (0.1.0)
Requirement already satisfied: pexpect; sys_platform != "win32" in /usr/local/lib/python3.6/dist-packages (from ipython==7.7.0) (4.7.0)
Requirement already satisfied: traitlets>=4.2 in /usr/local/lib/python3.6/dist-packages (from ipython==7.7.0) (4.3.2)
Requirement already satisfied: setuptools>=18.5 in /usr/local/lib/python3.6/dist-packages (from ipython==7.7.0) (41.2.0)
Requirement already satisfied: pygments in /usr/local/lib/python3.6/dist-packages (from ipython==7.7.0) (2.1.3)
Requirement already satisfied: pickleshare in /usr/local/lib/python3.6/dist-packages (from ipython==7.7.0) (0.7.5)
Requirement already satisfied: jedi>=0.10 in /usr/local/lib/python3.6/dist-packages (from ipython==7.7.0) (0.15.1)
Requirement already satisfied: wcwidth in /usr/local/lib/python3.6/dist-packages (from prompt-toolkit<2.1.0,>=2.0.0->ipython==7.7.0) (0.1.7)
Requirement already satisfied: six>=1.9.0 in /usr/local/lib/python3.6/dist-packages (from prompt-toolkit<2.1.0,>=2.0.0->ipython==7.7.0) (1.12.0)
Requirement already satisfied: ptyprocess>=0.5 in /usr/local/lib/python3.6/dist-packages (from pexpect; sys_platform != "win32"->ipython==7.7.0) (0.6.0)
Requirement already satisfied: ipython-genutils in /usr/local/lib/python3.6/dist-packages (from traitlets>=4.2->ipython==7.7.0) (0.2.0)
Requirement already satisfied: parso>=0.5.0 in /usr/local/lib/python3.6/dist-packages (from jedi>=0.10->ipython==7.7.0) (0.5.1)
ERROR: jupyter-console 5.2.0 has requirement prompt-toolkit<2.0.0,>=1.0.0, but you'll have prompt-toolkit 2.0.9 which is incompatible.
ERROR: google-colab 1.0.0 has requirement ipython~=5.5.0, but you'll have ipython 7.7.0 which is incompatible.
Installing collected packages: prompt-toolkit, ipython
  Found existing installation: prompt-toolkit 1.0.16
    Uninstalling prompt-toolkit-1.0.16:
      Successfully uninstalled prompt-toolkit-1.0.16
  Found existing installation: ipython 5.5.0
    Uninstalling ipython-5.5.0:
      Successfully uninstalled ipython-5.5.0
Successfully installed ipython-7.7.0 prompt-toolkit-2.0.9
```


# !curl https://cli-assets.heroku.com/install.sh | sh
Heroku CLI installation
```
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1892  100  1892    0     0  15636      0 --:--:-- --:--:-- --:--:-- 15636
Installing CLI from https://cli-assets.heroku.com/heroku-linux-x64.tar.xz
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 17.0M  100 17.0M    0     0  6341k      0  0:00:02  0:00:02 --:--:-- 6339k
v11.14.0
heroku installed to /usr/local/bin/heroku
heroku/7.29.0 linux-x64 node-v11.14.0
```



# !pip install pipenv  
!pipenv install  
!pipenv shell  
```
Collecting pipenv
  Downloading https://files.pythonhosted.org/packages/13/b4/3ffa55f77161cff9a5220f162670f7c5eb00df52e00939e203f601b0f579/pipenv-2018.11.26-py3-none-any.whl (5.2MB)
     |████████████████████████████████| 5.2MB 3.4MB/s 
Collecting virtualenv (from pipenv)
  Downloading https://files.pythonhosted.org/packages/f7/69/1ad2d17560c4fc60170056dcd0a568b83f3453a2ac91155af746bcdb9a07/virtualenv-16.7.4-py2.py3-none-any.whl (3.3MB)
     |████████████████████████████████| 3.3MB 42.3MB/s 
Collecting virtualenv-clone>=0.2.5 (from pipenv)
  Downloading https://files.pythonhosted.org/packages/ba/f8/50c2b7dbc99e05fce5e5b9d9a31f37c988c99acd4e8dedd720b7b8d4011d/virtualenv_clone-0.5.3-py2.py3-none-any.whl
Requirement already satisfied: certifi in /usr/local/lib/python3.6/dist-packages (from pipenv) (2019.6.16)
Requirement already satisfied: pip>=9.0.1 in /usr/local/lib/python3.6/dist-packages (from pipenv) (19.2.2)
Requirement already satisfied: setuptools>=36.2.1 in /usr/local/lib/python3.6/dist-packages (from pipenv) (41.2.0)
Installing collected packages: virtualenv, virtualenv-clone, pipenv
Successfully installed pipenv-2018.11.26 virtualenv-16.7.4 virtualenv-clone-0.5.3
/content/myproject
Creating a virtualenv for this project…
Pipfile: /content/myproject/Pipfile
Using /usr/bin/python3 (3.6.8) to create virtualenv…
⠙ Creating virtual environment...Already using interpreter /usr/bin/python3
Using base prefix '/usr'
New python executable in /root/.local/share/virtualenvs/myproject-5DVR_BVm/bin/python3
Also creating executable in /root/.local/share/virtualenvs/myproject-5DVR_BVm/bin/python
Installing setuptools, pip, wheel...
done.

✔ Successfully created virtual environment! 
Virtualenv location: /root/.local/share/virtualenvs/myproject-5DVR_BVm
Creating a Pipfile for this project…
Pipfile.lock not found, creating…
Locking [dev-packages] dependencies…
Locking [packages] dependencies…
Updated Pipfile.lock (ca72e7)!
Installing dependencies from Pipfile.lock (ca72e7)…
  🐍   ▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉ 0/0 — 00:00:00
To activate this project's virtualenv, run pipenv shell.
Alternatively, run a command inside the virtualenv with pipenv run.
```


# !ipython kernelspec list  
```   
[TerminalIPythonApp] WARNING | Subcommand `ipython kernelspec` is deprecated and will be removed in future versions.
[TerminalIPythonApp] WARNING | You likely want to use `jupyter kernelspec` in the future
Available kernels:
  ir         /usr/local/share/jupyter/kernels/ir
  python2    /usr/local/share/jupyter/kernels/python2
  python3    /usr/local/share/jupyter/kernels/python3
  swift      /usr/local/share/jupyter/kernels/swift
  ```   
