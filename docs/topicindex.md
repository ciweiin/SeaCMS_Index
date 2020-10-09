# 专题列表标签
```
参数:
size:每页数据条数 缺省值为12
{seacms:topicindexlist size=12}
[topicindexlist:i]专题排序位
[topicindexlist:n]专题排列位,永远都是从1开始
[topicindexlist:name]专题名称
[topicindexlist:count]专题包含的数据数量
[topicindexlist:pic]专题图片
[topicindexlist:link]专题链接
[topicindexlist:des]专题描述:可控制长度缺省为50
{/seacms:topicindexlist}
固定分页标签:
[topicindexlist:pagenumber len=10]
自定义分页标签：
{topicindexlist:pagenumber len=10}
[pagenumber:link]1.....10页链接
[pagenumber:page]页数字
{/topicindexlist:pagenumber}
{topicindexlist:page}当前页数
{topicindexlist:pagecount} 总页数
{topicindexlist:recordcount}总数据条数
{topicindexlist:firstlink}第一页链接
{topicindexlist:backlink} 上一页链接
{topicindexlist:nextlink} 下一页链接
{topicindexlist:lastlink} 最后一页链接
自定义分页范例：
{topicindexlist:page}/{topicindexlist:pagecount} 共{topicindexlist:recordcount}条记录
1..<
{topicindexlist:pagenumber len=8}
{if:{topicindexlist:page}<>[pagenumber:page]}
[pagenumber:page]{else}
[pagenumber:page]
{end if}
{/topicindexlist:pagenumber}
>
..{topicindexlist:pagecount}
```