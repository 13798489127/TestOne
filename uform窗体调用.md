# 窗体调用 U.UI.Form  \|\|  U.UI.From

---

解释：由于编写原因 U.UI.Form  和  U.UI.From 两函数写法等价，作用相同. 优选U.UI.Form写法

使用方法：U.UI.Form\({object}\);

参数说明：

```
{
    "min": 是否允许最小化, 默认允许

    "max" : 是否允许最大化, 默认允许

    "id": 窗体id,

    "style": 窗体样式, 形如{"属性名"："值"}

    "content": 内容, 

    "title": 标题,

    "hst": 标题区域设置, 形如Ufrom动态创建赋值属性方法

    "bst": 内容区域设置 形如Ufrom动态创建赋值属性方法

    "SO": 是否允许拉伸
}
```

示例：

```
U.UI.From({ id: "ufrom",
            style: {"background": "black"},
            content:"内容（innerHTML）",
            title: "标题",
            hst:{ "id": "hst",
                        "style": {"background": "white", "color": "black"}
            },
            bst: {"id": "cst",
                        "style": {"color":"red"}}
          });
```

窗体结构截图：

![](/Image/image094.png)

结果：

![](/Image/image093.png)

### 



