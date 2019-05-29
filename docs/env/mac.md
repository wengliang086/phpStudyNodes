## MAC 下 开发环境搭建

### 注意事项
1. Nginx 用户、权限问题

* https://www.jianshu.com/p/11e4e6726346
* https://www.cnblogs.com/meng1314-shuai/p/8335140.html
* https://blog.csdn.net/u012707422/article/details/84405349
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
