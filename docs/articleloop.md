# 文章单层循环标签
```
解析范围: 所有模板
参数:
num:数据条数缺省值为10
commend：推荐星级 1,2,3,4,5/all 可以调用单个、多个或全部星级缺省值为非推荐
order:数据排序方式id,按发布时间time,按点击量hit,按推荐commend,按顶次数digg,按随即random（慎用，可能造成卡顿），按当天点击量dayhit，按周点击量weekhit，按月点击量monthhit，总得分score 默认time
type:数据所在分类,可调出一个或多个分类数据,如 1,2,3/all缺省值为全部,在频道页值为current
time:数据发布时间,当天day 当周week 当月month 缺省值为无
start:数据列表调用的起点位置，缺省值为1
letter:数据名称的首字母，如letter=a
id:文章ID 35,6,7,58/all 默认为all
rel：rel=v相关视频,rel=n相关文章（利用该标签可以很方便的实现剧情、演员表、相关文章等功能，当视频的标题等于文章的关键词时，相关视频即可调用成功，当文章的关键词相同时，相关文章调用成功）
{seacms:newslist num=15 order=time type=all time=day start=5 letter=a id=35,6,7,58 }
[newslist:i]文章排列位
[newslist:n]文章排列位,永远都是从1开始
[newslist:id]文章实际id
[newslist:typename]分类中文名
[newslist:typelink]分类链接
[newslist:title len=10]文章标题 具有len属性控制长度,缺省为10
[newslist:colortitle len=3]文章标题:可控制长度 缺省为不控制
[newslist:note]文章属性,可配合标题一起显示
[newslist:newslink]文章内容页链接
[newslist:pic]图片
[newslist:author len=3]作者:可控制长度，缺省为不控制
[newslist:outline len=10]文章简述，可控制长度 缺省为不控制
[newslist:content]文章正文，文章标题 具有len属性控制长度,缺省为不控制
[newslist:hit]点击量
[newslist:time]文章添加时间,可控制时间格式yyyy-mm-dd yyyy-m-d yy-mm-dd mm-dd 缺省为mm-dd，如：[newslist:time style= yyyy-mm-dd]
[newslist:from]文章来源
[newslist:commend]文章推荐状态值
[newslist:letter]文章的首字母
[newslist:digg]顶次次数
[newslist:tread]踩次次数
[newslist:score]评分
[newslist:scorenum]评分总数
[newslist:scorenumer]评分总人数
{/seacms:newslist}
```