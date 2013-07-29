.. _api:

*********
API 客户端接口
*********

postlist 获取消息列表
===============

url:
----
   http://xxx/api/v1/postlist?from=xx&count=xx

HTTP请求方式:
---------
   GET
  
  

请求参数:
-----
* from:

   必选:可选
   
   类型:int   
 
   说明:参数为指定从第几条消息开始列出 (0为最新的第一条消息)
      
            默认为from=0 即从最新的消息开始列出

* count:

   必选:可选
   
   类型:int   
 
   说明:表示列出从from开始的多少条消息 (必须大于等于1)
   
            默认为count=20 即列出20条消息

返回数据:
-----

   列出公共消息的id, title,abstract,createtime,changetime,ownerid,默认按照changetime排序::

.. _making-a-table:

   ==============      ================   
      参数名称                      说明
   ==============      ================ 
   id                   消息的唯一标志符,对应获取具体内容的postid
   title                消息标题
   abstract             消息摘要
   createtime           消息创建时间
   changetime           消息最近一次的修改时间
   ownerid              消息发布者(拥有者)的id
   ==============      ================ 



示例:
---

   按照JSON格式显示::
   
      [{"id": 23, "title": "test for abstract again", "abstract": "test", 
      
      "createtime": "2013-07-22 14:49:41", "changetime": "2013-07-22 19:51:13", "ownerid": 4}, 
      
      {"id": 24, "title": "Tornado", "abstract": "", 
      
      "createtime": "2013-07-22 14:49:52", "changetime": "2013-07-22 14:49:52", "ownerid": 1}]


getpost 获取详细消息内容
================

url:
----
   http://xxx/api/v1/getpost?postid=xx

HTTP请求方式:
---------
   GET
  
  

请求参数:
-----
* postid:

   必选:必选
   
   类型:int   
 
   说明:postid为数据库中每条消息的唯一标识符
   
            如果消息删除或不存在这个postid则显示no post网页不指定postid则默认显示no post网页

返回数据:
-----

   获取具体的某条消息内容,生成简单的网页显示(网页本身支持responsive design)









