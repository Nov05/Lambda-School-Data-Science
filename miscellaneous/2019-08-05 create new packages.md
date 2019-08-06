2019-08-05  

https://packaging.python.org/tutorials/packaging-projects/  

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
(ds-unit3) PS D:\lambdaschool\python-packages\lambdata-nov05> python setup.py sdist bdist_wheel
running sdist
running egg_info
creating example_pkg_your_username.egg-info
writing example_pkg_your_username.egg-info\PKG-INFO
writing dependency_links to example_pkg_your_username.egg-info\dependency_links.txt
writing top-level names to example_pkg_your_username.egg-info\top_level.txt
writing manifest file 'example_pkg_your_username.egg-info\SOURCES.txt'
reading manifest file 'example_pkg_your_username.egg-info\SOURCES.txt'
writing manifest file 'example_pkg_your_username.egg-info\SOURCES.txt'
running check
creating example-pkg-your-username-0.0.1
creating example-pkg-your-username-0.0.1\example_pkg_your_username.egg-info
copying files to example-pkg-your-username-0.0.1...
copying README.md -> example-pkg-your-username-0.0.1
copying setup.py -> example-pkg-your-username-0.0.1
copying example_pkg_your_username.egg-info\PKG-INFO -> example-pkg-your-username-0.0.1\example_pkg_your_username.egg-info
copying example_pkg_your_username.egg-info\SOURCES.txt -> example-pkg-your-username-0.0.1\example_pkg_your_username.egg-info
copying example_pkg_your_username.egg-info\dependency_links.txt -> example-pkg-your-username-0.0.1\example_pkg_your_username.egg-info
copying example_pkg_your_username.egg-info\top_level.txt -> example-pkg-your-username-0.0.1\example_pkg_your_username.egg-info
Writing example-pkg-your-username-0.0.1\setup.cfg
creating dist
Creating tar archive
removing 'example-pkg-your-username-0.0.1' (and everything under it)
running bdist_wheel
running build
installing to build\bdist.win-amd64\wheel
running install
running install_egg_info
Copying example_pkg_your_username.egg-info to build\bdist.win-amd64\wheel\.\example_pkg_your_username-0.0.1-py3.7.egg-info
running install_scripts
adding license file "LICENSE" (matched pattern "LICEN[CS]E*")
creating build\bdist.win-amd64\wheel\example_pkg_your_username-0.0.1.dist-info\WHEEL
creating 'dist\example_pkg_your_username-0.0.1-py3-none-any.whl' and adding 'build\bdist.win-amd64\wheel' to it
adding 'example_pkg_your_username-0.0.1.dist-info/LICENSE'
adding 'example_pkg_your_username-0.0.1.dist-info/METADATA'
adding 'example_pkg_your_username-0.0.1.dist-info/WHEEL'
adding 'example_pkg_your_username-0.0.1.dist-info/top_level.txt'
adding 'example_pkg_your_username-0.0.1.dist-info/RECORD'
removing build\bdist.win-amd64\wheel
```

