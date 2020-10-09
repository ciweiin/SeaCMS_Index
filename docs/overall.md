# 全局标签
```
解析范围：以下标签无特殊说明的话、均支持所有模板
{seacms:top} 页面头部
{seacms:foot}页面尾部
{seacms:indexlink}首页链接
{seacms:topiclink}专题首页链接
{seacms:newslink} 文章首页链接
{seacms:gbook} 留言链接标签
{seacms:siteurl}网址，形如:www.seacms.net
{seacms:member} 会员登录，注册
{seacms:vipname} 会员用户名，静态模式无效 
{seacms:vipid} 会员id，静态模式无效
{seacms:vipgid} 会员用户组id，静态模式无效 
{seacms:sitepath}调用seacms的安装路径，安装路径可以在后台设置和修改。
{seacms:adfolder}网站广告文件夹名，广告文件夹位于根目录下的js文件夹中，默认ads
{seacms:sitename}调用seacms的站点名称，如站长设置站点名称为“seacms电影站”，那在模板中调用这个标签即可显示这个名字
{seacms:des} 站点描述
{seacms:copyright}管理员信箱---ICP备案信息--程序版本，支持html标签
{seacms:sitevisitjs}网站统计代码,如某网站的统计JS:<script language="javascript" type="text/javascript" src= "< /FONT>http://js.users.51.la/3400570.js"></script>
{seacms:sitenotice}网站关键词
{seacms:allcount} 网站总数据数量
{seacms:daycount} 当天更新数据数量
{seacms:keywords} 搜索关键字(后台设置)
{seacms:hotkeywords len=5}热门搜索关键字,可控制个数,默认为5个(搜索最多的关键字)
{seacms:runinfo}程序运行信息
{seacms:currenttypeid} 当前分类ID(注意:此标签只能在分类页、内容页、播放页有效,表示当前数据所在分类ID，在其他页为-444)
{seacms:letterlist} 首字母排序列表
{seacms:slide width=450 height=233} 幻灯片标签，width及height属性分别控制幻灯片宽度高度
{seacms:showhistory} 我的观看历史 显示/隐藏 功能按钮 必需调{seacms:maxhistory}盒子
{seacms:maxhistory width=960 height=190 num=10 style=pic} 观看历史盒子显示标签 width及height属性分别控制宽度高度,num显示条数,style样式(pic或font) 默认为pic
{seacms:strip}<html></html>{/seacms:strip} 移除html标签外多余的空格、换行符、制表符，起压缩网页大小作用，使网页打开更快
{seacms:load filename}载入附加模板 filename 是你的模板文件名
例1: 
{seacms:load head.html}效果跟{seacms:top}一样,载入附加模板head.html
```