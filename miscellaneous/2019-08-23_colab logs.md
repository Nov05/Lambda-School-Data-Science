
# !sudo apt purge python2.7-minimal
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
