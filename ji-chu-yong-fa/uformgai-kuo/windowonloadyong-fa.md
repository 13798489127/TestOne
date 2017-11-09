```
//两种写法：①原生的window.onload可用Uform写成$().onload(functoin(){})
```

```
            ②document.onready可用Uform写成$().ready(fucntion(){})
//这两个方法的效果都是一样的，都是在dom文档树加载完之后执行一个函数
（注意，这里面的文档树加载完不代表全部文件加载完）。
所以$().ready(fucntion(){}) 在文档树加载完之后 就可以执行了。
而window.onload是在dom文档树加载完和所有文件加载完之后执行一个函数。
也就是说$(document).ready要比window.onload先执行
```



