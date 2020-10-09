# 整体结构
```
（一）海洋cms的模板内的if判断支持一些PHP函数，如果你熟悉一些php编程技术，可以实现一些更加强大和灵活的功能。例如：
例如判断当天是星期几：{if:date('N')==2}周二{else}不是周二{end if}
这里就是使用了php时间函数 date('xxxxxx')的功能，其它参数请百度查阅php相关函数。
（二）评分 评论 顶踩 留言 幻灯片 定时任务等功能依赖系统js文件，模板必须引入以下js文件:
     <script>var sitePath= '{seacms:sitepath}';</script>
     <script src= "/{seacms:sitepath}js/common.js"></script>
     <script src= "/{seacms:sitepath}js/function.js"></script> 
（三）播放器调用必须引入play.js，播放页模板play.html的上面加入：
     <script src="/{seacms:sitepath}js/play.js"></script>
（四）关于点击数，内容页和播放页如果没有{playpage:hit} 点击数标签，则点击数无法增加
（五）收藏影片标签代码，当开启会员中心并已加载系统js的情况下，收藏代码如下：
     <a href="javascript:AddFav('影片id','')">收藏</a> （影片id请对应各个页面的id标签） 
（六）关于搜索的要点：
视频搜索对应文件：根目录/search.php，input的name值：searchword，action=search.php
文章搜索对应文件：根目录/so.php，input的name值：searchword，action=so.php
（七）关于自定义页面：自定义页面需要在后台生成才可以访问，用self_开头，用#表示存放的目录，默认根目录。
例如：self_new.html表示根目录下，self_top#new.html表示top文件夹下。
（八）对应的默认模板文件名称：
首页index.html
频道列表页channel.html
搜索列表页search.html
级联筛选列表页cascade.html
自定义页列表self_xxxx.html
文章首页newsindex.html
文章列表页newspage.html
文章搜索页newssearch.html
专题列表topicindex.html
专题页topic.html
内容页content.html
播放页play.html
弹出播放页openplay.html
文章内容页news.html
留言板gbook.html
tags页tag.html
视频地图页map.html
文章地图页newsmap.html
头部页面head.html
底部页面foot.html
用户注册reg.html
用户登录login.html
```