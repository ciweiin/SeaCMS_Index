# 视频单层循环标签
```
解析范围：所有模板
参数:
num:数据条数缺省值为10
state:连载影片调用条件 l表示连载,w为非连载,缺省值为全部
ver:视频版本，例如：ver=预告片
sid：按视频id调用视频，支持多个id，用英文逗号分开，如 sid=1,2,3,5,8
zt: 按专题id调用视频，仅支持一个id，如 zt=3 
commend：推荐星级 1,2,3,4,5/all 可以调用单个、多个或全部星级缺省值为非推荐
order:数据排序方式，id/idasc,按发布时间，time/timeasc，按年代year/yearasc，按评分次数scorenum/scorenumasc，按点击量hit/hitasc，dayhit日点击排序 weekhit周点击排序 monthhit月点击排序，按推荐commend/commendasc，按顶次数digg/diggasc，按随机random（慎用，可能造成卡顿），按评分score/douban/mtime/imdb，默认time。（其中带asc的为正序，不带asc的为倒序）
type:数据所在分类,可调出一个或多个分类数据,如 1,2,3/all缺省值为全部,在频道页值为current
time:数据发布时间,当天day 当周week 当月month 缺省值为无
start:数据列表调用的起点位置，缺省值为1
letter:数据名称的首字母，如letter=a
lang: 数据的语言
area:数据的地区
year:数据上映年份
jq:按剧情分类，如jq=爱情
reweek:按更新周期 
tvs:按上映电视台 
company:按制作公司
rel:相关资源调用，rel=v（仅在新闻内容页页有效，当新闻关键词等于视频名称时生效），rel=d为同导演影片，rel=y同演员，rel=r像似名称影片（利用该标签可以很方便的实现剧情、演员表、相关文章等功能，当文章的关键词等于视频标题时，相关文章即可调用成功）
{seacms:videolist num=15 order=time type=all commend=1,2,3 start=5 letter=a lang=英语 area=美国 year=2014}
[videolist:i]数据排列位
[videolist:n]排列位,不受start影响,永远都是从1开始数
[videolist:id]数据实际id
[videolist:typeid]数据所在分类实际id
[videolist:typename]数据分类中文名
[videolist:typelink]数据分类链接
[videolist:name len=3]数据名称:可控制长度 缺省为不控制
[videolist:note len=10]影片备注信息,可配合标题一起显示,可控制长度 缺省为不控制
[videolist:link]数据内容页链接
[videolist:playlink]数据播放页链接
[videolist:pic]图片
[videolist:spic]幻灯图片
[videolist:gpic]背景图片
[videolist:money]所需积分数
[videolist:actor len=3]主演:可控制长度，缺省为不控制
[videolist:nolinkactor]无链接主演:可控制长度，缺省为不控制
[videolist:hit]点击量
[videolist:dayhit]当日点击数
[videolist:weekhit]本周点击数
[videolist:monthhit]本月点击数
[videolist:nickname]影片别名
[videolist:reweek]更新周期
[videolist:vodlen]影片时长
[videolist:vodtotal]影片总集数
[videolist:douban]豆瓣评分
[videolist:mtime]时光网评分
[videolist:imdb]IMDB评分
[videolist:tvs]上映电视台
[videolist:company]发行公司
[videolist:des len=30]描述:可控制长度 缺省为字符长度50
[videolist:time style= yyyy-mm-dd]时间:可控制时间格式yyyy-mm-dd yy-mm-dd mm-dd 注：可选万能时间标签，详情查询php的date()函数或者gmdate() 函数
例如实现当日更新影片的时间显示为红色{if:"[videolist:timestyle=yyyy-mm-dd]"==date('Y-m-d')} color="red"{end if} >[videolist:time style=mm-dd]
[videolist:from]数据来源 如优酷、土豆
[videolist:commend]数据推荐状态值
[videolist:state]数据连载状态
[videolist:publishtime]数据发行年份
[videolist:ver]视频版本
[videolist:publisharea]数据发行地区
[videolist:playlink]数据播放页链接
[videolist:letter]数据名称的首字母 
[videolist:director]导演
[videolist:lang]语言
[videolist:colorname len=3]数据彩色名称:可控制长度 缺省为不控制
[videolist:digg]顶次次数
[videolist:tread]踩次次数
[videolist:keyword]设置的SEO关键字、支持超级链接模式，可以作为数据的TAG
[videolist:score]评分
[videolist:scorenum]评分总数
[videolist:scorenumer]评分总次数
[videolist:jqtype]剧情分类名称带链接
[videolist:nolinkjqtype]剧情分类名称不带链接
{/seacms:videolist}
```