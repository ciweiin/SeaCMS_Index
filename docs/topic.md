# 专题页标签
```
参数：
order数据排序方式，id/idasc,按发布时间，time/timeasc，按点击量hit/hitasc，按推荐commend/commendasc，按顶次数digg/diggasc，按随机random，按评分score/douban/mtime/imdb，默认time。（其中带asc的为正序，不带asc的为倒序）
{seacms:topicpagelist size=5 order=time}
[topicpagelist:i]数据排列位
[topicpagelist:id]数据实际id
[topicpagelist:typeid]数据所在分类实际id
[topicpagelist:typename]数据分类中文名
[topicpagelist:typelink]数据分类链接
[topicpagelist:name len=3]数据名称:可控制长度 缺省为不控制
[topicpagelist:note len=10]影片备注信息,可配合标题一起显示,可控制长度 缺省为不控制
[topicpagelist:link]数据内容页链接
[topicpagelist:pic]图片
[topicpagelist:spic]幻灯图片
[topicpagelist:gpic]背景图片
[topicpagelist:money]所需积分数
[topicpagelist:actor len=3]主演:可控制长度，缺省为不控制
[topicpagelist:hit]点击量
[topicpagelist:dayhit]当日点击数
[topicpagelist:weekhit]本周点击数
[topicpagelist:monthhit]本月点击数
[topicpagelist:score]评分
[topicpagelist:scorenum]评分总数
[topicpagelist:scorenumer]评分总人数
[topicpagelist:nickname]影片别名
[topicpagelist:reweek]更新周期
[topicpagelist:vodlen]影片时长
[topicpagelist:vodtotal]影片总集数
[topicpagelist:douban]豆瓣评分
[topicpagelist:mtime]时光网评分
[topicpagelist:imdb]IMDB评分
[topicpagelist:tvs]上映电视台
[topicpagelist:company]发行公司
[topicpagelist:des len=30]描述:可控制长度 缺省为字符长度50
[topicpagelist:time style= yyyy-mm-dd]时间:可控制时间格式yyyy-mm-ddyy-mm-dd mm-dd 缺省为yyyy-m-d 注：可选万能时间标签，详情查询php的date()函数或者gmdate() 函数
[topicpagelist:from]数据来源 如优酷、土豆
[topicpagelist:commend]数据推荐状态值
[topicpagelist:state]数据连载状态
[topicpagelist:publishtime]数据发行年份
[topicpagelist:ver]视频版本
[topicpagelist:publisharea]数据发行地区
[topicpagelist:playlink]数据播放页链接
[topicpagelist:letter]数据名称的首字母
[topicpagelist:colorname len=3]数据彩色名称:可控制长度 缺省为不控制
[topicpagelist:director]导演
[topicpagelist:lang]语言
[topicpagelist:digg]顶次次数
[topicpagelist:tread]踩次次数
[topicpagelist:keyword]设置的SEO关键字、支持超级链接模式，可以作为数据的TAG
[topicpagelist:jqtype]剧情分类名称带链接
[topicpagelist:nolinkjqtype]剧情分类名称不带链接
{/seacms:topicpagelist}
固定分页标签：
[topicpagelist:pagenumber len=10]
自定义分页标签：
{topicpagelist:pagenumber len=10}
[pagenumber:link]1.....10页链接
[pagenumber:page]页数字
{/topicpagelist:pagenumber}
{topicpagelist:page}当前页数
{topicpagelist:pagecount} 总页数
{topicpagelist:recordcount}总数据条数
{topicpagelist:firstlink}第一页链接
{topicpagelist:backlink} 上一页链接
{topicpagelist:nextlink} 下一页链接
{topicpagelist:lastlink} 最后一页链接
自定义分页范例：
{topicpagelist:page}/{topicpagelist:pagecount} 共{topicpagelist:recordcount}条记录
1..<
{topicpagelist:pagenumber len=8}
{if:{topicpagelist:page}<>[pagenumber:page]}
[pagenumber:page]{else}
[pagenumber:page]
{end if}
{/topicpagelist:pagenumber}
>
..{topicpagelist:pagecount}
独有标签：
{seacms:topicname} ：专题名称
{seacms:topicdes} ：专题介绍
{seacms:topickeyword} ： 专题关键词
{seacms:currrent_topic_id} : 当前专题id
{seacms:topicpic} ：专题图片
```