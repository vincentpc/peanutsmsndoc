.. _installation-and-configuaration:


**************************************
Installation and Configuration 系统安装及运行
**************************************

.. _installation

Installation 安装
===============

.. _dependency

Dependency
----------

.. _making-a-list:

* Python 2.7::

    http://www.python.org/download/releases/2.7/
    
* Mysql::

    sudo apt-get install mysql
    sudo apt-get install mysql-dev

* Mysql-python::

    pip install mysql-python

* Tornado::
 
    pip install tornado


.. note::
   利用requirement.txt可自动安装mysql-python,tornado
    
   pip install -r requirement.txt
   
.. _install

Install
-------

.. _making-a-list:

* 解压缩::

   tar xvzf webcontentvXX.tar.gz  

* 进入目录::

   cd webcontentvXX     

* 设置参数(初次运行前设置一次即可,详细介绍见下文)::

   vi conf.py           

* 运行::

   python web.py          

.. _configuration


Configuration 配置
================

.. _database-config:

Database Configuration
----------------------

使用sqlconfig文件下的sql脚本创建数据库

默认创建名字为WEBPOSTV1的数据库,如果存在则会删除后创建

默认USER有一个root账户(帐户密码均为root) 登录后可修改密码::

   Mysql -uname -ppassword < CreateDatabase.sql  

.. _config:

Configuration
-------------
初始设置参数说明(conf.py)::

    #######################
    # system Configure ##
    #######################
    #初始运行时设置cookie加密密钥,任意字符串
    COOKIE_SECRET =  'mynameisvincentchan' 
    #初始运行时设置关闭http服务器缓冲时间,默认3秒
    MAX_WAIT_SECONDS_BEFORE_SHUTDOWN = 3
    
    
    #######################
    # Database Configure ##
    #######################
    
    #数据库连接设置,以此为IP,端口,用户名,用户密码,数据库名称
    DB_HOST = '10.0.2.15' 
    DB_PORT = 3306
    DB_USER = 'admin'
    DB_PASSWD = '123456'
    DB_NAME = 'MSNV1'





　　　



