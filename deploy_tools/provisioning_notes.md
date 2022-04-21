配置新网站
=================================

## 需要的包

* nginx
* Python 3.6
* virtualenv + pip
* Git

以Ubuntu为例：
    sudo add-apt-repository ppa:fkrull/deadsnakes
    sudo apt-get install nginx git python36 python3.6-venv

## Nginx 虚拟机

* 参考nginx.template.conf
* 把SITENAME替换成所需的域名，例如staging.my-domain.com

## Systemd服务

* 参考gunicorn-upstart.template.conf
* 把SITENAME替换成所需的域名，例如stagin.my-domain.com

## 文件夹架构
假设有用户账户， 家目录为/home/username

/home/username
└─ sites
    └─ SITENAME
        ├─ database
        ├─ source
        ├─ static
        └─ virtualenv