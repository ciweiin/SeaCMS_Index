# 文章搜索页列表
```
参数:
size:每页条数默认值10
order:数据排序方式id/time/hit 缺省值为time
{seacms:newssearchlist size=15}
[newssearchlist:i]文章排列位
[newssearchlist:id]文章实际id
[newssearchlist:typename]分类中文名
[newssearchlist:typelink]分类链接
[newssearchlist:title len=10]文章标题 具有len属性控制长度,缺省为10
[newssearchlist:colortitle len=3]文章标题:可控制长度 缺省为不控制
[newssearchlist:note]文章属性,可配合标题一起显示
[newssearchlist:link]文章内容页链接
[newssearchlist:pic]图片
[newssearchlist:author len=3]作者:可控制长度，缺省为不控制
[newssearchlist:outline len=10]文章简述，可控制长度 缺省为不控制
[newssearchlist:content]文章正文，文章标题 具有len属性控制长度,缺省为不控制
[newssearchlist:hit]点击量
[newssearchlist:time]文章添加时间,可控制时间格式yyyy-mm-dd yy-mm-dd mm-dd 缺省为yyyy-m-d
[newssearchlist:from]文章来源
[newssearchlist:commend]文章推荐状态值
[newssearchlist:letter]文章的首字母
[newssearchlist:digg]顶次次数
[newssearchlist:tread]踩次次数
[newssearchlist:score]评分
[newssearchlist:scorenum]评分总数
[newssearchlist:scorenumer]评分总人数
{/seacms:newssearchlist}
固定分页标签：
[newssearchlist:pagenumber len=8]
自定义分页标签：
{newssearchlist:pagenumber len=10}
[pagenumber:link]1.....10页链接
[pagenumber:page]页数字
{/newssearchlist:pagenumber}
{newssearchlist:page}当前页数
{newssearchlist:pagecount} 总页数
{newssearchlist:recordcount}总数据条数
{newssearchlist:firstlink}第一页链接
{newssearchlist:backlink} 上一页链接
{newssearchlist:nextlink} 下一页链接
{newssearchlist:lastlink} 最后一页链接
自定义分页范例：
{newssearchlist:page}/{newssearchlist:pagecount} 共{newssearchlist:recordcount}条记录
1..<
{newssearchlist:pagenumber len=8}
{if:{newssearchlist:page}<>[pagenumber:page]}
[pagenumber:page]{else}
[pagenumber:page]
{end if}
{/newssearchlist:pagenumber}
>
..{newssearchlist:pagecount}
独有标签：
{seacms:newssearchword} 搜索关键词
{seacms:newssearchnum} 搜索结果数
```