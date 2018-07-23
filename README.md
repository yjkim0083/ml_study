# 밑바닥부터 시작하는 머신러닝 실습환경 구성
## Miniconda
![](https://conda.io/docs/_images/conda_logo.svg)
- [download - 공식사이트](https://conda.io/miniconda.html)
- 다운받은 exe 파일 실행, 모든건 기본으로 설정하고 설치

### 가상환경 설정
- window > Anaconda prompt
- 가상환경 생성

```shell
(base) C:\Users\XXX>conda create -n ml_scratch python=3.7
Solving environment: done

The following packages will be downloaded:

package                    |            build
---------------------------|-----------------
vc-14.1                    |       h0510ff6_3           5 KB
setuptools-39.2.0          |           py37_0         570 KB
wheel-0.31.1               |           py37_0          80 KB
wincertstore-0.2           |           py37_0          13 KB
vs2015_runtime-15.5.2      |                3         2.2 MB
pip-10.0.1                 |           py37_0         1.7 MB
python-3.7.0               |       hea74fb7_0        21.1 MB
certifi-2018.4.16          |           py37_0         142 KB
------------------------------------------------------------
                                        Total:        25.9 MB

The following NEW packages will be INSTALLED:

certifi:        2018.4.16-py37_0
pip:            10.0.1-py37_0
python:         3.7.0-hea74fb7_0
setuptools:     39.2.0-py37_0
vc:             14.1-h0510ff6_3
vs2015_runtime: 15.5.2-3
wheel:          0.31.1-py37_0
wincertstore:   0.2-py37_0

Proceed ([y]/n)? y
Downloading and Extracting Packages
vc-14.1              |    5 KB | ############################################################################## | 100%
setuptools-39.2.0    |  570 KB | ############################################################################## | 100%
wheel-0.31.1         |   80 KB | ############################################################################## | 100%
wincertstore-0.2     |   13 KB | ############################################################################## | 100%
vs2015_runtime-15.5. |  2.2 MB | ############################################################################## | 100%
pip-10.0.1           |  1.7 MB | ############################################################################## | 100%
python-3.7.0         | 21.1 MB | ############################################################################## | 100%
certifi-2018.4.16    |  142 KB | ############################################################################## | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate ml_scratch
#
# To deactivate an active environment, use
#
#     $ conda deactivate
```
- 가상환경 실행
```shell
(base) C:\Users\XXX>conda activate ml_scratch
```

## jupyter, pandas, numpy, matplotlib 설치
### jupyter
```shell
(ml_scratch) C:\Users\XXX>conda install jupyter
```

### pandas, numpy
- pandas를 설치하면 numpy도 같이 설치됨

```shell
(ml_scratch) C:\Users\XXX>conda install pandas
```

### matplotlib
```shell
(ml_scratch) C:\Users\XXX>conda install matplotlib
```

### 설치확인
- python shell 에서 설치한 라이브러리들을 import 해본다

```shell
(ml_scratch) C:\Users\XXX>python
Python 3.6.6 |Anaconda, Inc.| (default, Jun 28 2018, 11:27:44) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import numpy
>>> import pandas
>>> import matplotlib
>>>
```

## jupyter 실행
- 실행하고자 하는 폴더에 가서 실행
```shell
(ml_scratch) C:\dev\python>jupyter notebook
[I 14:23:25.473 NotebookApp] Writing notebook server cookie secret to C:\Users\김용주\AppData\Roaming\jupyter\runtime\notebook_cookie_secret
[I 14:23:25.744 NotebookApp] Serving notebooks from local directory: C:\dev\python
[I 14:23:25.745 NotebookApp] The Jupyter Notebook is running at:
[I 14:23:25.748 NotebookApp] http://localhost:8888/?token=768afe2c93a6028e383e8dccd95d652da4263e8bc4cb4826
[I 14:23:25.748 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 14:23:25.754 NotebookApp]

    Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://localhost:8888/?token=768afe2c93a6028e383e8dccd95d652da4263e8bc4cb4826
[I 14:23:25.935 NotebookApp] Accepting one-time-token-authenticated connection from ::1
```
