2019-08-05   

** Windows 10, Anaconda3**  

## Anaconda Power Shell

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
