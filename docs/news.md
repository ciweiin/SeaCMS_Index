# 文章内容页标签
```
{news:textlink} 文章内容页的当前位置
{news:id} 文章ID
{news:upid} 文章父分类ID
{news:note} 文章属性,可配合标题一起显示
{news:link} 文章内链接地址
{news:url} 文章外链接地址
{news:typeid} 文章分类ID
{news:title len=10}文章标题,具有len属性控制长度,缺省为不控制
{news:outline} 文章简述，具有len属性控制长度,缺省为不控制
{news:author} 作者
{news:from} 来源
{news:pic} 图片地址
{news:addtime} 时间
{news:addtime2}百度SEO格式时间，输出格式为：2018-07-12T01:17:33
{news:content} 文章正文 具有len属性控制长度,缺省为不控制
{news:commend} 文章星级数字,推荐值为1-5,不推荐为0,例{if:{news:commend}>0}推荐文章{end if}
{news:typename} 分类中文名称
{news:hit} 文章点击率
{news:prenext} 上一个下一个文章标签
{news:pre} 上一个新闻 单独标签
{news:next} 下一个新闻 单独标签
{news:comment} 评论标签
{news:marklen=10}评分标签，len=10 0到10分评分项，style=star 星星评分样式
{news:digg} 顶标签,显示顶数目及顶操作
{news:tread} 踩标签,显示踩数目及踩操作
{news:diggnum} 顶标签,只显示顶数字
{news:treadnum} 踩标签,只显示踩数字
{news:score} 评分，直接显示数字
{news:scorenum} 评分总数
{news:scorenumer} 评分总人数
{news:keywords} 文章设置的SEO关键字、支持超级链接模式，可以作为数据的TAG
{news:nolinkkeywords}文章设置的SEO关键字,无链接
{news:encodetitle}URL编码的文章标题 用来传递URL参数
{news:subtitle} 分页副标题
{news:subcontent}文章正文包含分页符（#p#副标题#e#） 进行内容分页 
{news:subpagenumber len=10} 分页数字列表 len表示数字列表长度
注：新闻内容页可以利用循环标签{seacms:videolist rel=v}来实现调用相关视频，当新闻关键词等于视频名称时，自动调用对应视频。
```