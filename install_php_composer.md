### in windows

##### 获取composer 资源

* 1.download by url [composer](https://getcomposer.org/Composer-Setup.exe)
* 2.install by terminal

> cd your_file
>
> php -r "readfile('https://getcomposer.org/installer');" | php
> 
> echo @php "%~dp0composer.phar" %*>composer.bat

##### test

> composer -V
> Composer version 27d8904

#### 考虑到网络问题可以需要修改镜像

* 1.修改全局配置

> composer config -g repo.packagist composer https://packagist.phpcomposer.com

* 2.修改制定的composer.json

> "repositories": {
>    "packagist": {
>        "type": "composer",
>        "url": "https://packagist.phpcomposer.com"
>    }
> }
