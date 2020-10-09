# 自定义页列表标签
```
解析范围：自定义模板
参数:
size:每页显示数据条数 缺省为10
maxpage:最多生产页数，不填写为只生成1页
order:数据排序方式，id/idasc,按发布时间，time/timeasc，按点击量hit/hitasc，dayhit日点击排序 weekhit周点击排序 monthhit月点击排序，按推荐
commend/commendasc，按顶次数digg/diggasc，按随机random，按评分score/douban/mtime/imdb，默认time。（其中带asc的为正序，
不带asc的为倒序）
type:数据所在分类,可调出一个或多个分类数据,如 1,2,3/all缺省值为全部，必须是最终分
类，不要填写无内容的父分类
letter:数据名称的首字母，如letter=a
lang: 数据的语言
area:数据的地区
year:数据上映年份
jq:数据的剧情分类值
{seacms:customvideolist size=5 maxpage=10 order=time letter=a area=美国 jq=动作}
[customvideolist:i]数据排列位
[customvideolist:id]数据实际id
[customvideolist:typeid]数据所在分类实际id
[customvideolist:typename]数据分类中文名
[customvideolist:typelink]数据分类链接
[customvideolist:name len=3]数据名称:可控制长度 缺省为不控制
[customvideolist:note len=10]影片备注信息,可配合标题一起显示,可控制长度 缺省为不控制
[customvideolist:link]数据内容页链接
[customvideolist:pic]图片
[customvideolist:spic]幻灯图片
[customvideolist:gpic]背景图片
[customvideolist:money]所需积分数
[customvideolist:actor len=3]主演:可控制长度，缺省为不控制
[customvideolist:hit]点击量
[customvideolist:dayhit]当日点击数
[customvideolist:weekhit]本周点击数
[customvideolist:monthhit]本月点击数
[customvideolistscore]评分
[customvideolistscorenum]评分总数
[customvideolist:scorenumer]评分总人数
[customvideolist:nickname]影片别名
[customvideolist:reweek]更新周期
[customvideolist:vodlen]影片时长
[customvideolist:vodtotal]影片总集数
[customvideolist:douban]豆瓣评分
[customvideolist:mtime]时光网评分
[customvideolist:imdb]IMDB评分
[customvideolist:tvs]上映电视台
[customvideolist:company]发行公司
[customvideolist:des len=30]描述:可控制长度 缺省为字符长度50
[customvideolist:time style= yyyy-mm-dd]时间:可控制时间格式yyyy-mm-ddyy-mm-dd mm-dd 缺省为yyyy-m-d 注：可选万能时间标签，详情查询php的date()函数或者gmdate() 函数
[customvideolist:from]数据来源 如优酷、土豆
[customvideolist:commend]数据推荐状态值
[customvideolist:state]数据连载状态
[customvideolist:publishtime]数据发行年份
[customvideolist:ver]视频版本
[customvideolist:publisharea]数据发行地区
[customvideolist:playlink]数据播放页链接
[customvideolist:letter]数据名称的首字母
[customvideolist:colorname len=3]数据彩色名称:可控制长度 缺省为不控制
[customvideolist:director]导演
[customvideolist:lang]语言
[customvideolist:digg]顶次次数
[customvideolist:tread]踩次次数
[customvideolist:keyword]设置的SEO关键字、支持超级链接模式，可以作为数据的TAG
[customvideolist:jqtype]剧情分类名称带链接
[customvideolist:nolinkjqtype]剧情分类名称不带链接
{/seacms:customvideolist}
固定分页标签：
[customvideolist:pagenumber len=10]
自定义分页标签：
{customvideolist:pagenumber len=10}
[pagenumber:link]1.....10页链接
[pagenumber:page]页数字
{/customvideolist:pagenumber}
{customvideolist:page}当前页数
{customvideolist:pagecount} 总页数
{customvideolist:recordcount}总数据条数
{customvideolist:firstlink}第一页链接
{customvideolist:backlink} 上一页链接
{customvideolist:nextlink} 下一页链接
{customvideolist:lastlink} 最后一页链接
自定义分页范例：
{customvideolist:page}/{customvideolist:pagecount} 共{customvideolist:recordcount}条记录
1..<
{customvideolist:pagenumber len=8}
{if:{customvideolist:page}<>[pagenumber:page]}
[pagenumber:page]{else}
[pagenumber:page]
{end if}
{/customvideolist:pagenumber}
>
..{customvideolist:pagecount}
```