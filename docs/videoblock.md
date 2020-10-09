# 视频区域块列表标签
```
视频区域块列表标签arealist
解析范围：所有模板
参数:
areatype:区域块列表分别调用的数据分类值为1,2,3/all支持单个或多个,多个分类逗号隔开;all调出全部一级分类的区域列表块
例:
{seacms:arealist areatype=1,2,6}或者{seacms:arealist letter=a,b,c,d}
[arealist:i]区域块排序位
[arealist:typename]区域块中类型的名称
[arealist:count]区域块数据数量
[arealist:link]区域块分类链接
{seacms:videolist num=5 order=time type=areatype time=all tart=1}
或者{seacms:videolist num=5 order=time letter=[arealist:typename]time=all start=1}
-------内部内部标签参考videolist标签用法------
{/seacms:videolist}
{/seacms:arealist}
```