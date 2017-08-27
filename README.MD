## 概述
当前 Dockerfile 制作的是 nginx 、php-fpm 环境
* 基于 alpine:3.4 制作的镜像
* 已经集成git client环境，支持 git 代码更新部署【git pull、 git push】
* 容器也可以更新模版文件中的变量
* 支持 lets encrypt SSL 的配置，自定义 nginx 配置，php 配置
* 容器内的 用户，可以通过 uid 方式映射出来
* 其他安装程序 vim 编辑器、composer、


### 版本信息
| Docker Tag | GitHub Release | Nginx Version | PHP Version | Alpine Version |
|-----|-------|-----|--------|--------|
| latest | Master Branch |1.13.4 | 7.1.8 | 3.4 |

### 友情连接（参考）
- [https://github.com/ngineered/nginx-php-fpm](https://github.com/ngineered/nginx-php-fpm)
- [https://registry.hub.docker.com/u/richarvey/nginx-php-fpm/](https://registry.hub.docker.com/u/richarvey/nginx-php-fpm/)

## 快速开始


## nginx 配置文件
* nginx的错误页面，如果需修改的话
 404页面配置 ./errors:/var/www/errors
 
 
## php 配置文件
- php配置文件         /usr/local/etc/php/conf.d/docker-vars.ini
- php-fpm 配置        /usr/local/etc/php-fpm.d/

## 重启php
supervisorctl restart php-fpm

## 重启 nginx
supervisorctl restart nginx