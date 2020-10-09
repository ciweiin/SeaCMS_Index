# 内容页播放页标签
```
解析范围：以下标签无特殊说明的话,均支持内容页、播放页模板
{playpage:textlink}内容页或播放页的当前位置
{playpage:id} ID
{playpage:upid}父分类ID
{playpage:typeid}分类ID
{playpage:name} 名称,具有len属性控制长度,缺省为不控制
{playpage:encodename} 片名的urlencode,传递URL参数用的
{playpage:link}内链接地址
{playpage:playlink} 立即播放链接地址
{playpage:url} 外链接地址
{playpage:publishtime} 发行年份
{playpage:ver} 视频版本
{playpage:publisharea} 发行地区
{playpage:actor}有链接地址主演,具有len属性控制长度,缺省为不控制
{playpage:nolinkactor} 无链接地址数据主演,具有len属性控制长度,缺省为不控制,可以作为内容页或播放页的页面描述
{playpage:director} 带链接导演
{playpage:nolinkdirector} 不带链接导演信息
{playpage:pic} 图片
{playpage:spic} 幻灯图片
{playpage:gpic} 背景图片
{playpage:money} 所需积分数
{playpage:addtime}更新时间
{playpage:addtime2}百度SEO格式时间，输出格式为：2018-07-12T01:17:33
{playpage:state}连载状态,显示连载到的数字,非连载为0,例{if:{playpage:state}==0}完结{else}更新至{playpage:state}集{end if}
{playpage:des} 介绍,具有len属性控制长度,配合len属性可以作为内容页或播放页的页面描述,缺省为不控制
{playpage:commend}推荐星级数字,推荐值为1-5,不推荐为0,例{if:{playpage:commend}>0}推荐数据{end if}
{playpage:typename}分类中文名称
{playpage:typelink} 分类链接
{playpage:note} 备注,可以配合标题一起显示,具有len属性控制长度,缺省为不控制,例{if:"{playpage:note}"<>""}{playpage:note}{end if}
{playpage:lang} 语言
{playpage:playurlinfo} 播放地址数据信息,供播放器调用(必须在{playpage:player}标签前调用),仅支持播放页模板
{playpage:player}播放器调用标签,仅支持播放页
{playpage:from} 某来源名称
{playpage:dz} 播放地址
{playpage:part} 某集名称标签
{playpage:hit} 人气，模板里如没有这个标签，则点击数无法增加
{playpage:dayhit} 当日点击数
{playpage:weekhit} 本周点击数
{playpage:monthhit} 本月点击数
{playpage:nickname} 影片别名
{playpage:reweek} 更新周期
{playpage:vodlen} 影片时长
{playpage:vodtotal} 影片总集数
{playpage:douban} 豆瓣评分
{playpage:mtime} 时光网评分
{playpage:imdb} IMDB评分
{playpage:tvs} 上映电视台
{playpage:company} 发行公司 
{playpage:reporterr} 报错标签 
rel:相关资源，仅内容页和播放页有效，rel=d为同导演影片，rel=y同演员，rel=r像似名称影片,使用办法查看seacms：videolist标签里的对应说明
{playpage:prenext}上一个下一个视频标签，内容页跳至内容页，播放页跳至播放页
{playpage:pre} 上一个视频 单独标签，内容页跳至内容页，播放页跳至播放页
{playpage:next} 下一个视频 单独标签 ，内容页跳至内容页，播放页跳至播放页
{playpage:preplaylink}上一集 播放链接
{playpage:nextplaylink}下一集 播放链接
{playpage:comment}评论标签
{playpage:keywords}设置的SEO关键字、支持超级链接模式，可以作为数据的TAG
{playpage:nolinkkeywords}设置的SEO关键字
{playpage:jqtype} 剧情分类名称带链接
{playpage:nolinkjqtype} 剧情分类名称不带链接
{playpage:director}有链接地址导演
{playpage:nolinkdirector}无链接地址数据导演,可以作为内容页或播放页的页面描述
{playpage:desktopurl} 下载快捷方式到桌面链接
{playpage:mark len=10} 评分标签，len=10 0到10分评分项，style=star 星星评分样式
{playpage:digg} 顶标签,显示顶数目及顶操作
{playpage:tread}踩标签,显示踩数目及踩操作
{playpage:diggnum}顶标签,只显示顶数字
{playpage:treadnum}踩标签,只显示踩数字
{playpage:score}评分，直接显示数字
{playpage:scorenum}评分总数
{playpage:scorenumer}评分总人数
{playpage:playlistlen}播放列表总组数 需放在播放列表后
{playpage:downlistlen} 下载列表总组数  需放在下载列表后
{playpage:longtxt}备用说明，支持长文本内容
播放列表标签:
{playpage:playlist}
[playlist:i]播放地址实际序号，不随着来源排序变化
[playlist:s]播放来源排序数值，显示后台你设置的播放来源排列序号
[playlist:link target=_self]播放地址链接，以多个li方式输出, target:链接打开方式,当前_self 新窗口_blank 顶部_top 缺省值为_blank
[playlist:url]播放列表实际播放地址 带链接
[playlist:nolinkurl]播放列表实际播放地址 不带链接
[playlist:from]播放来源名称，如优酷、土豆
[playlist:ename]播放来源英文名称，如youku、tudou
[playlist:intro]播放格式说明，如QVOD数据显示为：需要下载QVOD播放器，点此下载播放器
{/playpage:playlist}
下载列表标签：
{playpage:downlist}
[downlist:i]下载地址排列位
[downlist:link]下载地址链接, target:链接打开方式,当前_self 新窗口_blank 顶部_top 缺省值为_blank
[downlist:linkstr]实际下载地址
[downlist:from]下载来源
{/playpage:downlist}
```