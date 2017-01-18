# RadioList列表

---

使用方法：U.UI.RadioList\(d,s\)

参数一：生成checkbox的父亲元素,通常为一个div元素。

参数二：json格式

例：

```
var d=$$("div",{},document.body);//创建一个放置Radio的div元素。

var ra = U.UI.RadioList(d,{"TW":"提问","ZY":"作业","JH":"精华","CT":"控件"});
```

结果：

![](/Image/image101.png)

注：ra.value保存了用户选中Radio的值。

