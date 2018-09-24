# python下载地址
` https://www.python.org/downloads/windows/`  
[本示例下载安装 python-3.7.0-amd64.exe] ***注意安装64位python***  
安装成功后添加环境变量  
`C:\Users\stoplyy\AppData\Local\Programs\Python\Python37`


# pip 下载地址
` https://pypi.org/project/pip/#files` 
[本示例下载安装 pip-18.0.tar.gz]   
下载成功解压后进入 setup.py 文件所在目录  
输入install命令安装  
```
PS C:\Users\stoplyy\Downloads\pip-18.0\pip-18.0> python setup.py install
..安装输出...
Processing pip-18.0-py3.7.egg
creating c:\users\stoplyy\appdata\local\programs\python\python37\lib\site-packages\pip-18.0-py3.7.egg
Extracting pip-18.0-py3.7.egg to c:\users\stoplyy\appdata\local\programs\python\python37\lib\site-packages
Adding pip 18.0 to easy-install.pth file
Installing pip-script.py script to C:\Users\stoplyy\AppData\Local\Programs\Python\Python37\Scripts
Installing pip.exe script to C:\Users\stoplyy\AppData\Local\Programs\Python\Python37\Scripts
Installing pip3-script.py script to C:\Users\stoplyy\AppData\Local\Programs\Python\Python37\Scripts
Installing pip3.exe script to C:\Users\stoplyy\AppData\Local\Programs\Python\Python37\Scripts
Installing pip3.7-script.py script to C:\Users\stoplyy\AppData\Local\Programs\Python\Python37\Scripts
Installing pip3.7.exe script to C:\Users\stoplyy\AppData\Local\Programs\Python\Python37\Scripts

Installed c:\users\stoplyy\appdata\local\programs\python\python37\lib\site-packages\pip-18.0-py3.7.egg
Processing dependencies for pip==18.0
Finished processing dependencies for pip==18.0
```
最后的安装输出中显示将pip 安装到`C:\Users\stoplyy\AppData\Local\Programs\Python\Python37\Scripts`目录  
将此目录添加到Path  
```
--查看pip版本
PS C:\Users\stoplyy\Downloads\pip-18.0\pip-18.0> pip -V
pip 18.0 from c:\users\stoplyy\appdata\local\programs\python\python37\lib\site-packages\pip-18.0-py3.7.egg\pip (python 3.7)
```
# Kear安装

##  Theano 安装
`pip install -U Theano`
## Tensorflow 安装
```
PS C:\Users\stoplyy\Downloads\pip-18.0\pip-18.0> pip3 install --upgrade tensorflow

--如果提示No matching 采用源安装模式
Collecting tensorflow
  Could not find a version that satisfies the requirement tensorflow (from versions: )
No matching distribution found for tensorflow

python -m pip install --upgrade https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-0.12.0-py3-none-any.whl
```


MinGw

MINGW_HOME = C:/MinGW
LIBRARY_PATH = %MINGW_HOME%/lib
C_INCLUDE_PATH = %MINGW_HOME%/include
CPLUS_INCLUDE_PATH = %MINGW_HOME%/include/c++/3.4.5;%MINGW_HOME/include/c++/3.4.5/mingw32;%MINGW_HOME/include/c++/3.4.5/backward;%MINGW_HOME%/include
path=%path%;%MINGW_HOME%/bin