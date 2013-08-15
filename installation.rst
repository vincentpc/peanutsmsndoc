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

 参考网址 `Python 2.7 <http://www.python.org/download/releases/2.7/>`_

* Mysql::

    sudo apt-get install mysql
    sudo apt-get install mysql-dev
    
 参考网址 `mysql <http://www.mysql.com/>`_

* Mysql-python::

    pip install mysql-python

 参考网址 `MySQL for Python <http://sourceforge.net/projects/mysql-python/>`_

* Tornado::
 
    pip install tornado
    
 参考网址 `Tornado <http://www.tornadoweb.cn/>`_

* jinja2::
 
    pip install jinja2
    
 参考网址 `Jinja2 <http://jinja.pocoo.org/docs/#>`_
 
.. note::
   make init 自动安装依赖软件(jinja2,tornado,mysql-python)
   
   make doc  自动生成使用文档,文档目录在doc/_build下
       
.. _install

Install
-------

.. _making-a-list:


* 进入目录::

   cd peanuts     

* 初次运行创建数据库(/etc/CreateDatabase.sql)::

   mysql -uname -ppassword < CreateDatabase.sql      
   
* 初次运行设置参数(设置一次即可,详细介绍见下文)::

   vi config.py            

* 运行::
   
   python app.py          

.. _configuration


Configuration 配置
================

.. _database-config:

Database Configuration
----------------------

使用peanuts/etc文件下的sql脚本创建数据库

默认创建名字为PEANUTS的数据库,如果存在则会删除后创建

默认USER有一个管理员账户(帐户密码均为root) 登录后可修改密码::

.. _config:

System Configuration
--------------------
初始设置系统参数说明(config.py)::

    #######################
    # system Configure ##
    #######################
    #初始运行时设置cookie加密密钥,任意字符串
    COOKIE_SECRET =  'mynameisvincentchan' 
    #初始运行时设置关闭http服务器缓冲时间,默认1秒
    MAX_WAIT_SECONDS_BEFORE_SHUTDOWN = 1
    
    
    #######################
    # Database Configure ##
    #######################
    
    #数据库连接设置,依次为IP,端口,用户名,用户密码,数据库名称
    DB_HOST = '10.0.2.15' 
    DB_PORT = 3306
    DB_USER = 'xxxx'
    DB_PASSWD = 'xxxx'
    DB_NAME = 'PEANUST'

Log
---
存储在log文件夹下::





　　　



