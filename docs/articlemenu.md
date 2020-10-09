# 文章菜单列表标签
```
文章菜单列表标签newsmenulist及newssmallmenulist
解析范围：支持所有模板
参数:
type:菜单类型：1,2,3/all/top1,2,3表示分类ID支持单个或多个分类、多个分类用逗号隔开,top表示调出一级菜单,all全部调出分类菜单(ulliulli)
注意：
1.此标签支持双层循环嵌套，newsmenulist内嵌smallnewsmenulist，如下例3
2.newsmenulist的type表示分类id(smallnewsmenulist的type表示父级分类的ID）
例1:
{seacms:menulist by=news type=top}
[menulist:i]菜单项排序位
[menulist:typename]菜单项名称
[menulist:typeid]菜单项id
[menulist:upid]父级菜单项id
[menulist:link]菜单项链接
{/seacms:menulist}
例2:
同时调出一级分类和二级分类
{seacms:menulist type=top by=news}[menulist:typename]{/seacms:menulist}
{seacms:menulist type=son by=news}[menulist:typename]{/seacms:menulist}
例3:
循环调出一级分类及二级分类
{seacms:menulist type=top by=news}
[menulist:typename]
{seacms:smallmenulist by=news type=[menulist:typeid]}
[smallmenulist :typename]
{/seacms:smallmenulist}
{/seacms:menulist}
例4：{seacms:menulist by=news type=1,2,3,4}
[menulist:typename]
{/seacms:menulist}
```