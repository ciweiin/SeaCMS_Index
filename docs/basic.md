# 基础语法
```
海洋cms模板标签类似于XML格式，所有的模板都含有定界符，
默认情况下是{seacms:*}和{/seacms:*}，“*”代表模板标记名称。


一般情况下{seacms:*}和{/seacms:*}是成对出现的
例如：
{seacms:videolist num=5}
<h2><a href="[videolist:link]">[videolist:name]</a></h2>
<p>[videolist:des]...<a href="[videolist:link]">[打开]</a></p>
{/seacms:videolist}
上面的{seacms:arclist}和{/seacms:arclist}成对出现在模板文件中。


标签还有一类出现形式是{seacms:*}，通常以这种形式出现都是输出变量、或者不含底层模板的内容。
例如：
{seacms:sitename} 站点名称
{seacms:des} 站点描述
{seacms:sitenotice}网站关键词

```