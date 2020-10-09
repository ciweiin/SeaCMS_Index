# 文章列表页标签
```
参数:
size:每页条数默认值10
order:数据排序方式id/time/hit 缺省值为time
{seacms:newspagelist size=15}
[newspagelist:i]文章排列位
[newspagelist:id]文章实际id
[newspagelist:typename]分类中文名
[newspagelist:typelink]分类链接
[newspagelist:title len=10]文章标题 具有len属性控制长度,缺省为10
[newspagelist:colortitle len=3]文章标题:可控制长度 缺省为不控制
[newspagelist:note]文章属性,可配合标题一起显示
[newspagelist:link]文章内容页链接
[newspagelist:pic]图片
[newspagelist:author len=3]作者:可控制长度，缺省为不控制
[newspagelist:outline len=10]文章简述，可控制长度 缺省为不控制
[newspagelist:content]文章正文，文章标题 具有len属性控制长度,缺省为不控制
[newspagelist:hit]点击量
[newspagelist:time]文章添加时间,可控制时间格式yyyy-mm-dd yy-mm-dd mm-dd 缺省为yyyy-m-d
[newspagelist:from]文章来源
[newspagelist:commend]文章推荐状态值
[newspagelist:letter]文章的首字母
[newspagelist:digg]顶次次数
[newspagelist:tread]踩次次数
[newspagelist:score]评分
[newspagelist:scorenum]评分总数
[newspagelist:scorenumer]评分总人数
{/seacms:newspagelist}
固定分页标签：
[newspagelist:pagenumber len=8]
自定义分页标签：
{newspagelist:pagenumber len=10}
[pagenumber:link]1.....10页链接
[pagenumber:page]页数字
{/newspagelist:pagenumber}
{newspagelist:page}当前页数
{newspagelist:pagecount} 总页数
{newspagelist:recordcount}总数据条数
{newspagelist:firstlink}第一页链接
{newspagelist:backlink} 上一页链接
{newspagelist:nextlink} 下一页链接
{newspagelist:lastlink} 最后一页链接
自定义分页范例：
{newspagelist:page}/{newspagelist:pagecount} 共{newspagelist:recordcount}条记录
1..<
{newspagelist:pagenumber len=8}
{if:{newspagelist:page}<>[pagenumber:page]}
[pagenumber:page]{else}
[pagenumber:page]
{end if}
{/newspagelist:pagenumber}
>
..{newspagelist:pagecount}
独有标签：
{newspagelist:typename} 分类名称
{newspagelist:keywords}分类关键词
{newspagelist:description}分类简介
```