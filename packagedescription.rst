.. _pakage-description:


****************
Layout 工程文件分布及说明
****************



.. _making-a-list:


* app:

    逻辑层:响应不同URL的handler 
    
    (根据权限不同的操作,分别放在admin,editor,api三个文件夹中)
  
* model:

    数据库相关的函数方法,与数据库相关的增删查改方法放在dbapi.py中
    
* static: 

   显示层,静态显示的CSS,JS文件
   
   Ckeditor为消息内容发布的内容编辑器
   
* template:

    显示层,动态显示的html文件
    
    根据交互的对象不同分为admin edtior两个文件夹
    
* log:  

   运行时候的产生的log信息记录
   
 * tests:  

   测试文档

* doc:  

   开发及使用文档(本网站源代码)
       
* conf.py:  

    全局配置文件(数据库配置,服务器配置)
    
* web.py:

    服务器启动文件
    
* sqlconfig:      

    初始建立数据库文件
    
* README:  

    项目说明文档









　　　



