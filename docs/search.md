# 搜索列表页标签
```
参数：
size:每页数据条数 缺省值为12
order:数据排序方式，id/idasc,按发布时间，time/timeasc，按点击量hit/hitasc，按推荐commend/commendasc，按顶次数digg/diggasc，按随机random，默认time。（其中带asc的为正序，不带asc的为倒序）
{seacms:searchlist size=5 order=time}
[searchlist:i]数据排列位
[searchlist:id]数据实际id
[searchlist:typeid]数据所在分类实际id
[searchlist:typename]数据分类中文名
[searchlist:typelink]数据分类链接
[searchlist:name len=3]数据名称:可控制长度 缺省为不控制
[searchlist:note len=10]影片备注信息,可配合标题一起显示，可控制长度 缺省为不控制
[searchlist:link]数据内容页链接
[searchlist:pic]图片
[searchlist:spic]幻灯图片
[searchlist:gpic]背景图片
[searchlist:money]所需积分数
[searchlist:actor len=3]主演:可控制长度 缺省为不控制
[searchlist:hit]点击量
[searchlist:dayhit]当日点击数
[searchlist:weekhit]本周点击数
[searchlist:monthhit]本月点击数[searchlist:score]评分
[searchlist:scorenum]评分总数
[searchlist:scorenumer]评分总人数
[searchlist:nickname]影片别名
[searchlist:reweek]更新周期
[searchlist:vodlen]影片时长
[searchlist:vodtotal]影片总集数
[searchlist:douban]豆瓣评分
[searchlist:mtime]时光网评分
[searchlist:imdb]IMDB评分
[searchlist:tvs]上映电视台
[searchlist:company]发行公司
[searchlist:des len=30]描述:可控制长度缺省为50
[color=red[searchlist:time style= yyyy-mm-dd]时间:可控制时间格式yyyy-mm-ddyy-mm-dd mm-dd 缺省为yyyy-m-d注：可选万能时间标签，详情查询php的date()函数或者gmdate() 函数
[searchlist:from]数据来源 如优酷、土豆
[searchlist:state]数据连载状态值
[searchlist:commend]数据推荐状态值
[searchlist:publishtime]数据发行年份
[searchlist:ver]视频版本
[searchlist:publisharea]数据发行地区
[searchlist:playlink]数据播放页链接
[searchlist:colorname len=3]数据彩色名称:可控制长度 缺省为不控制
[searchlist:director]导演
[searchlist:lang]语言
[searchlist:digg]顶次次数
[searchlist:tread]踩次次数
[searchlist:keyword]设置的SEO关键字、支持超级链接模式，可以作为数据的TAG
[searchlist:jqtype]剧情分类名称带链接
[searchlist:nolinkjqtype]剧情分类名称不带链接
{/seacms:searchlist}
固定分页标签：
[searchlist:pagenumber len=10]
自定义分页标签：
{searchlist:pagenumber len=10}
[pagenumber:link]1.....10页链接
[pagenumber:page]页数字
{/searchlist:pagenumber}
{seacms:searchword}搜索关键字名称
{seacms:searchnum}搜索结果的数目
{searchlist:page}当前页数
{searchlist:pagecount}总页数
{searchlist:recordcount} 总数据条数
{searchlist:firstlink}第一页链接
{searchlist:backlink}上一页链接
{searchlist:nextlink}下一页链接
{searchlist:lastlink}最后一页链接
自定义分页范例：
{searchlist:page}/{searchlist:pagecount} 共{searchlist:recordcount}条记录
1..<
{searchlist:pagenumber len=8}
{if:{searchlist:page}<>[pagenumber:page]}
[pagenumber:page]{else}
[pagenumber:page]
{end if}
{/searchlist:pagenumber}
>
..{searchlist:pagecount}
独有标签：
{seacms:searchword} 搜索关键字名称
{seacms:searchnum} 搜索结果的数目
{searchpage:ordername}搜索索引页当前排序方式标签
{searchpage:order-xxx-link} 搜素页排序方式链接标签，xxx可以为以下字段：id/idasc按照id排序，time/timeasc按时间排序 hit/hitasc按点击排序 commend/commendasc 按推荐星级排序 score/scoreasc按评分排序。（其中带asc的为正序，不带asc的为倒序）
```