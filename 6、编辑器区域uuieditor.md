# 编辑器区域

---

窗体编辑器

适用范围：博客发帖，论坛发帖，word编辑区域的公有属性

使用方法：U.UI.Editor\(obj\);

参数：

```
相关属性,形如：{

                    id：表示窗口唯一id

                    head：true是否显示功能区域默认不显示

                    isc：暂不了解

                    name：编辑器窗体名

                    title：标题（主题）

                    context：内容

                    fcb：回调函数

               }
```

示例：

```
Test = function () { alert() }

U.UI.Editor({ id: "aa", 
              head: true, 
              name: "编辑器窗体名", 
              title: "标题（主题）", 
              context: "内容",
              "fcb": U.M.apply(null, [[Test]]) 
              });
```

返回窗体：

![](/Image/image100.png)

非窗体编辑器

适用范围：博客发帖，论坛发帖，word编辑区域的公有属性

使用方法：U.UI.Editor\(obj\);

参数：

```
相关属性,形如：{

                    id：表示窗口唯一id

                    head：true是否显示功能区域默认不显示

                    isc：暂不了解

                    name：编辑器窗体名

                    title：标题（主题）

                    context：内容

                    fcb：回调函数
                    
                    parentEle : $("#parentEle")[0]

               }
```

```

```



