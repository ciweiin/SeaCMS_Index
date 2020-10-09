# 频道列表页标签
```
参数:
size:每页数据条数 缺省值为12
order:数据排序方式，id/idasc,按发布时间，time/timeasc，按点击量hit/hitasc，按推荐commend/commendasc，按顶次数digg/diggasc，按随机random，默认time。（其中带asc的为正序，不带asc的为倒序）
{seacms:channellist size=10 order=time}
[channellist:i]数据排列位
[channellist:id]数据实际id
[channellist:typeid]数据所在分类实际id
[channellist:typename]数据分类中文名
[channellist:typelink]数据分类链接
[channellist:name len=3]数据名称:可控制长度 缺省为不控制
[channellist:colorname len=3]数据彩色名称:可控制长度 缺省为不控制
[channellist:note len=10]影片备注信息,可配合标题一起显示，可控制长度 缺省为不控制
[channellist:link]数据内容页链接
[channellist:pic]图片
[channellist:spic]幻灯图片
[channellist:gpic]背景图片
[channellist:money]所需积分数
[channellist:actor len=3]主演:可控制长度 缺省为不控制
[channellist:nolinkactor]主演：无链接格式
[channellist:hit]点击量
[channellist:dayhit]当日点击数
[channellist:weekhit]本周点击数
[channellist:monthhit]本月点击数
[channellist:nickname]影片别名
[channellist:reweek]更新周期
[channellist:vodlen]影片时长
[channellist:vodtotal]影片总集数
[channellist:douban]豆瓣评分
[channellist:mtime]时光网评分
[channellist:imdb]IMDB评分
[channellist:tvs]上映电视台
[channellist:company]发行公司
[channellist:des len=30]描述:可控制长度缺省为50
[channellist:time style=yyyy-mm-dd]时间:可控制时间格式yyyy-mm-dd yy-mm-ddmm-dd 缺省为yyyy-m-d 注：可选万能时间标签，详情查询php的date()函数或者gmdate() 函数
[channellist:from]数据来源 如优酷、土豆
[channellist:state]数据连载状态值
[channellist:commend]数据推荐状态值
[channellist:publishtime]数据发行年份
[channellist:ver]视频版本
[channellist:publisharea]数据发行地区
[channellist:playlink]数据播放页链接 
[channellist:director]导演
[channellist:lang]语言
[channellist:digg]顶次次数
[channellist:tread]踩次次数
[channellist:keyword]设置的SEO关键字、支持超级链接模式，可以作为数据的TAG
[channellist:score]评分
[channellist:scorenum]评分总数
[channellist:scorenumer]评分总人数
[channellist:jqtype]剧情分类名称带链接
[channellist:nolinkjqtype]剧情分类名称不带链接
{/seacms:channellist}
固定分页标签：
[channellist:pagenumber len=10]
自定义分页标签：
{channellist:pagenumber len=10}
[pagenumber:link]1.....10页链接
[pagenumber:page]页数字
{/channellist:pagenumber}
{channellist:page}当前页数
{channellist:pagecount}总页数
{channellist:recordcount} 总数据条数
{channellist:firstlink}第一页链接
{channellist:backlink}上一页链接
{channellist:nextlink}下一页链接
{channellist:lastlink}最后一页链接
自定义分页范例：
{channellist:page}/{channellist:pagecount} 共{channellist:recordcount}条记录
1..<
{channellist:pagenumber len=8}
{if:{channellist:page}<>[pagenumber:page]}
[pagenumber:page]{else}
[pagenumber:page]
{end if}
{/channellist:pagenumber}
>
..{channellist:pagecount}
独有标签：
{channelpage:typeid} 当前分类id
{channelpage:typename} 当前分类中文名称
{channelpage:typetext} 频道页当前位置
{channelpage:title} 频道列表页seo标题
{channelpage:keywords} 频道模板MATH关键词
{channelpage:description} 频道模板MATH描述
{channelpage:order-xxx-link} 分类页排序方式链接标签，xxx可以为以下字段：id/idasc按照id排序，time/timeasc按时间排序 hit/hitasc按点击排序 commend/commendasc 按推荐星级排序 score/scoreasc按评分排序。（其中带asc的为正序，不带asc的为倒序）
```