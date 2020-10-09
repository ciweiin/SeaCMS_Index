# 专题调用标签
```
参数:
id:all表示调出所有专题;id为指定专题ID表示调出某个专题;调出指定多个专题使用英文逗号隔开;默认值为all
num:专题条数缺省值为10
start:专题列表调用的起点位置，缺省值为1
{seacms:topiclist id=all num=10 start=2}
[topiclist:i]专题排序位
[topiclist:n]专题排列位,永远都是从1开始
[topiclist:id]专题ID
[topiclist:name]专题名称
[topiclist:count]专题包含的数据数量
[topiclist:pic]专题图片
[topiclist:link]专题链接
[topiclist:des]专题描述:可控制长度缺省为50
{/seacms:topiclist}
```