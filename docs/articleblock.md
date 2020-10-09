# 文章区域块列表标签
```
解析范围：所有模板
参数:
areatype:区域块列表分别调用的数据分类值为1,2,3/all支持单个或多个,多个分类逗号隔开;all调出全部一级分类的区域列表块
例:
{seacms:newsarealist areatype=all}
[arealist:i]区域块排序位
[arealist:typename]区域块中类型的名称
[arealist:count]区域块数据数量
[arealist:link]区域块分类链接
{seacms:newslist num=40 order=time type=areatype}
-------内部内部标签参考newslist标签用法------
{/seacms:newslist}
{/seacms:newsarealist}
```