配置新网站
====================

## 需要的包：

* nginx
* Python3.6
* virtualenv + pip
* Git

以Ubuntu为例：

    sudo add-apt-repository ppa:fkrull/deadsnakes
    sudp apt install nginx git python36 python3.6-venv

## Nginx虚拟主机

* 参考nginx.template.conf
* 把SITENAME替换成所需的域名，例如 staging.my-domain.com

## Systemd服务

* 参考gunicorn-upstart.template.conf
* 把SITENAME替换成所需的域名，例如 staging.my-domain.com

## 文件夹结构：
假设没有用户账户，家目录为 /home/username

/home/username └── sites    ├── DOMAIN1    │ ├── db.sqlite3    │ ├── manage.py etc    │ ├── static    │ └── virtualenv    └── DOMAIN2    ├── db.sqlite3    ├── manage.py etc