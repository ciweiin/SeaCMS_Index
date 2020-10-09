# IF判断标签
```
支持php语句、多elseif判断
注意：使用==表示等于
解析范围：
支持所有模板,支持在所有循环列表标签中使用if标签,在if标签中可以使用嵌套if标签subif标签例1:
{if:[videolist:i]% 2==0}......{subif:[videolist:i]% 3==0}......{end subif}......{end if}
例2:
{if:[videolist:i]% 2==0}......{else}......{end if}
例3:
{if:[videolist:i]% 2==0}......{elseif:[videolist:i]% 3==0}......{elseif:[videolist:i]% 4==0}......{else}......{end if}
```