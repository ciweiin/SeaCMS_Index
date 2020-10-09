# 级联筛选列表页标签
```
参数：
size:每页数据条数 缺省值为12
order:数据排序方式，id/idasc,按发布时间，time/timeasc，按点击量hit/hitasc，按推荐commend/commendasc，按顶次数digg/diggasc，按随机random，默认time。（其中带asc的为正序，不带asc的为倒序）
{seacms:cascadelist size=5 order=time}
[cascadelist:i]数据排列位
[cascadelist:id]数据实际id
[cascadelist:typeid]数据所在分类实际id
[cascadelist:typename]数据分类中文名
[cascadelist:typelink]数据分类链接
[cascadelist:name len=3]数据名称:可控制长度 缺省为不控制
[cascadelist:note len=10]影片备注信息,可配合标题一起显示，可控制长度 缺省为不控制
[cascadelist:link]数据内容页链接
[cascadelist:pic]图片
[cascadelist:spic]幻灯图片
[cascadelist:gpic]背景图片
[cascadelist:money]所需积分数
[cascadelist:actor len=3]主演:可控制长度 缺省为不控制
[cascadelist:hit]点击量
[cascadelist:dayhit]当日点击数
[cascadelist:weekhit]本周点击数
[cascadelist:monthhit]本月点击数
[cascadelist:score]评分
[cascadelist:scorenum]评分总数
[cascadelist:scorenumer]评分总人数
[cascadelist:nickname]影片别名
[cascadelist:reweek]更新周期
[cascadelist:vodlen]影片时长
[cascadelist:vodtotal]影片总集数
[cascadelist:douban]豆瓣评分
[cascadelist:mtime]时光网评分
[cascadelist:imdb]IMDB评分
[cascadelist:tvs]上映电视台
[cascadelist:company]发行公司
[cascadelist:des len=30]描述:可控制长度缺省为50
[color=red[cascadelist:time style= yyyy-mm-dd]时间:可控制时间格式yyyy-mm-ddyy-mm-dd mm-dd 缺省为yyyy-m-d注：可选万能时间标签，详情查询php的date()函数或者gmdate() 函数
[cascadelist:from]数据来源 如优酷、土豆
[cascadelist:state]数据连载状态值
[cascadelist:commend]数据推荐状态值
[cascadelist:publishtime]数据发行年份
[cascadelist:ver]视频版本
[cascadelist:publisharea]数据发行地区
[cascadelist:playlink]数据播放页链接
[cascadelist:colorname len=3]数据彩色名称:可控制长度 缺省为不控制
[cascadelist:director]导演
[cascadelist:lang]语言
[cascadelist:digg]顶次次数
[cascadelist:tread]踩次次数
[cascadelist:keyword]设置的SEO关键字、支持超级链接模式，可以作为数据的TAG[cascadelist:jqtype]剧情分类名称带链接
[cascadelist:nolinkjqtype]剧情分类名称不带链接
{/seacms:cascadelist}
固定分页标签:
[cascadelist:pagenumber len=10]
自定义分页标签：
{cascadelist:pagenumber len=10}
[pagenumber:link]1.....10页链接
[pagenumber:page]页数字
{/cascadelist:pagenumber}
{seacms:searchword}搜索关键字名称
{seacms:searchnum}搜索结果的数目
{cascadelist:page}当前页数
{cascadelist:pagecount}总页数
{cascadelist:recordcount} 总数据条数
{cascadelist:firstlink}第一页链接
{cascadelist:backlink}上一页链接
{cascadelist:nextlink}下一页链接
{cascadelist:lastlink}最后一页链接
自定义分页范例：
{cascadelist:page}/{cascadelist:pagecount} 共{cascadelist:recordcount}条记录
1..<
{cascadelist:pagenumber len=8}
{if:{cascadelist:page}<>[pagenumber:page]}
[pagenumber:page]{else}
[pagenumber:page]
{end if}
{/cascadelist:pagenumber}
>
..{cascadelist:pagecount}
独有标签：
{seacms:searchnum}：搜索结果的数目
{searchpage:letter}：高级搜索当前选中的首字母
{searchpage:year}：高级搜索当前选中的年份
{searchpage:money}：高级搜索当前选中的收费情况
{searchpage:area}：高级搜索当前选中的地区
{searchpage:lang}：高级搜索当前选中的语言
{searchpage:type}：高级搜索当前选中的分类ID
{searchpage:typename}：高级搜索当前选中的分类名
{searchpage:state}：高级搜索当前选中的连载状态
{searchpage:ver}：高级搜索当前选择的视频版本
{searchpage:jq}：高级搜索当前选择的剧情分类
{searchpage:ordername}搜索索引页当前排序方式标签
{searchpage:ordername}搜索索引页当前排序方式标签
{searchpage:order-xxx-link}分类页排序方式链接标签，xxx可以为以下字段：id/idasc按照id排序，time/timeasc按时间排序 hit/hitasc按点击排序 commend/commendasc 按推荐星级排序 score/scoreasc按评分排序。（其中带asc的为正序，不带asc的为倒序）
独有条件筛选标签:分类条件标签（cascade.html）
type可为all,top或者其他分类id,多个id请用','隔开
{seacms:typeitemlist type=all}
[typeitemlist:tid]
[typeitemlist:link]
[typeitemlist:value]
{/seacms:typeitemlist}
地区条件标签(cascade.html):
{seacms:areaitemlist}
[areaitemlist:link]
[areaitemlist:value]
{/seacms:areaitemlist}
年份条件标签(cascade.html):
{seacms:yearitemlist}
[yearitemlist:link]
[yearitemlist:value]
{/seacms:yearitemlist}
首字母条件标签(cascade.html):
{seacms:letteritemlist}
[letteritemlist:link]
[letteritemlist:value]
{/seacms:letteritemlist}
语言条件标签(cascade.html):
{seacms:langitemlist}
[langitemlist:link]
[langitemlist:value]
{/seacms:langitemlist}
收费条件标签(cascade.html):
{seacms:moneyitemlist}
[moneyitemlist:link]
[moneyitemlist:value]
{/seacms:moneyitemlist}
剧情分类条件标签(cascade.html):
{seacms:jqitemlist}
[jqitemlist:link]
[jqitemlist:value]
{/seacms:jqitemlist}
连载状态条件标签(cascade.html):
{seacms:stateitemlist}
[stateitemlist:link]
[stateitemlist:value]
{/seacms:stateitemlist}
视频版本条件标签(cascade.html):
{seacms:veritemlist}
[veritemlist:link]
[veritemlist:value]
{/seacms:veritemlist}
```