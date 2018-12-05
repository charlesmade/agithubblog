### windows

##### 可以参考[windows-proxy](https://github.com/charlesmade/script-tools/blob/master/windows/set_proxy.bat)

> set https_proxy=example.com:port

> set http_proxy=example.com:port

or example

> set https_proxy=127.0.0.1:1080

> set http_proxy=127.0.0.1:1080

这里我使用了自己本地的sock5代理,监听本机1080端口

##### Test

> curl.exe http://ip.gs

> Current IP / 当前 IP: you now ip

> set_proxy // put set order 这是我自己编写的简陋的脚本[windows-proxy](https://github.com/charlesmade/script-tools/blob/master/windows/set_proxy.bat)

> curl.exe http://ip.gs

> Current IP / 当前 IP: ip has changed

### linux

##### 需要本地的一个代理服务,这里我是用的是自己本机的ss代理

> sudo vim /etc/profile

添加以下两行

> alias setproxy="export ALL_PROXY=socks5://127.0.0.1:1080"

> alias unsetproxy="unset ALL_PROXY"

保存然后

> source /etc/profile

##### Test

> curl http://ip.gs

> Current IP / 当前 IP: you now ip

> setproxy //引入配置

> curl http://ip.gs

> Current IP / 当前 IP: ip has changed

> unsetproxy //删除配置

> curl http://ip.gs

> Current IP / 当前 IP: you now ip
