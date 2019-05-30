## MAC 下 开发环境搭建

### 注意事项
1. Nginx 用户、权限问题

* MacOSX搭建PHP开发环境 https://www.jianshu.com/p/11e4e6726346
* mac下安装nginx https://www.cnblogs.com/meng1314-shuai/p/8335140.html
* Mac安装Nginx及使用中遇到的坑 https://blog.csdn.net/u012707422/article/details/84405349
* https://blog.csdn.net/tjcyjd/article/details/50897959
* https://segmentfault.com/a/1190000002797601

```shell
sudo chown root:wheel /usr/local/Cellar/nginx/1.2.6/bin/nginx
sudo chmod u+s /usr/local/Cellar/nginx/1.2.6/bin/nginx
```

2. Php-fpm 中配置用户、组

3. 对于 " location -》 root html；" 为什么找不到 html文件夹的问题

* 因为 /usr/local/Cellar/nginx/1.15.3/html 链接 到了 /usr/local/var/www/
* html -> ../../../var/www


### 默认软件位置

1. PHP

    1. executable目录：/usr/bin/php
    2. /private/etc/php/php.ini
    3. /private/etc/php/php-fpm.conf
    4. /private/etc/php-fpm.d/www.conf
2. Apache

    1. 配置文件：/private/etc/apache2/httpd.conf
    2. 部署路径：/Library/WebServer/Documents/
3. Nginx 
    
    1. 配置目录：/usr/local/etc/nginx/nginx.conf
    2. root目录：/usr/local/var/www/
    3. 安装目录：/usr/local/Cellar/nginx/1.15.3/

### swoole 安装

    1. https://linkeddestiny.gitbooks.io/easy-swoole/content/book/chapter01/install.html
    2. ./configure --prefix=/usr/local/php -enable-fpm --enable-sockets --enable-mbstring=all --with-config-file-path=/etc/php --with-openssl=/usr/local/Cellar/openssl/1.0.2p/ --with-curl=/usr/local/Cellar/curl/7.65.0/
    3. 