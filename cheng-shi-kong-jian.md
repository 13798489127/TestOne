# 分页控件

---

```js
U.PG.PPage(ParentElement, TotalLength, PageNum, DataNum, {

    "isp": 5, 

    "fun": [[fun,([page])]], 

    "page": [0]

} );
```

参数一（ParentElement）：添加分页控件的父亲元素

参数二（TotalLength）：数据总长度

参数三（PageNum）：当前为第几页

参数四（DataNum）：一页数据的数量

参数五（json）：键值一（"isp"）：显示的页数，左右对称显示

     如：5 表示左右个显示5个数字页

键值二（fun）：\[\[fun，\(\[page\]\)\]\]

参数（fun） ： 回调函数

参数（page）：页码

键值三（"page"）：\[page\]

参数一（page）：回调函数中，修改页数的参数位置 从0开始

示例：

```js
U.test = function (page){

        document.body.innerHTML ="";

        U.PG.PPage(document.body,20,page,5,{

                "isp":5,

                "fun":[[function(Page){U.test(Page);},([1])]],

                "page":[0]
        });
}
```

运行：

U.test\(0\);

页面示例：

![](/assets/import.png)

