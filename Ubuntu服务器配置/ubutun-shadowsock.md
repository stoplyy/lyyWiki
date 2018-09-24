#  Ubuntu-Shadowsocks 配置

安装Shadowsocks  
~~~
sudo apt-get install python-dev python-pip
sudo pip install shadowsocks
~~~
编写config文件
~~~
# shadowsocks_config.json
{
    "server":"×",
    "server_port":×,
    "local_address":"127.0.0.1",
    "local_port":1080,
    "password":"×",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open":false
}
~~~
运行
~~~
sudo sslocal -c shadowsocks_config.json
~~~
- 或者后台运行
~~~
sudo sslocal -c shadowsocks_config.json -d start
~~~
- 关闭后台运行
~~~
sudo sslocal -c shadowsocks_config.json -d stop
~~~
- 开机运行
~~~
vim /etc/rc.local
    /usr/local/bin/sslocal -c shadowsocks_config.json -d start
~~~


设置Sock全局代理
~~~
System Settings => Network => Network Proxy => Manual => Socks Host: 127.0.0.1:1080
~~~

配置Http代理

~~~
sudo apt-get install polipo

vim /etc/polipo/config
    socksParentProxy = "localhost:1080"
    socksProxyType = socks5

sudo service polipo restart

export http_proxy=http://localhost:8123
~~~
设置Http全局代理
~~~
    System Settings => Network => Network Proxy => Manual => Http Host: 127.0.0.1:8123 & Https Host: 127.0.0.1:8123
~~~

配置ssh使用Http代理
~~~
sudo apt-get install connect-proxy

vim /etc/ssh/ssh_config
    Host *
    ProxyCommand connect -H localhost:8123 %h %p

~~~