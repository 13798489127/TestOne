# 概括

```
在网页中拥有成百上千甚到上万的元素，而在这么庞大的元素群中，选取所要的元素是很多项目中的难题，
使用javascript中自带的document.getElementById等此类函数就可以在许多元素中找到所要的元素，
但这种最为基础的选取函数始终是不适合广大javascript程序员的使用的，我们的项目也一样,所以在通过研究Jquery
中神奇的选择器内核后，模仿编写出来的选择器函数，更利于我们在项目网页中更快的选取我们所需要的元素，此选择
器是基于document.getElementById()、getElementsByTagName()等函数编写的，
更利于我们筛选网页中的元素。下面我们就来看一下选择器的使用。
```

# 怎么使用? 添加一个必要文件!

## 如何获取对象?\($\)

```
<script src="http://www.1473.cn/uform.js"></script>
<script>

            #id             $("#usestudio")[0]          id=" usestudio " 的元素
            .class          $(".intro")[0]              className包含"intro" 的元素
            element         $("p")                      所有<p>标签元素
            @attr           $("@window")                所有包含window属性的元素
            @attr=val       $("@window=true")           所有包含window属性且=true的元素
            element>id      $("div>usestudio")          所有<div >id="usestudio"的元素
            ~Name           $("~name")                  所有name="green"的元素

</script>
```

## 元素的快速赋值\(addAttrArray\)

```
<script>

$().addAttrArray(AttrArray);
//选取元素后进行addAttrArray() 函数操作
$(“#window”).addAttrArray({“id” : ”id1”, “style” : {“left” : “100px”, “display” : “block” }});
//style中的属性不属于元素，所以在赋值left，display等样式属性时要在”style” : { 样式属性放在这儿 }

</script>
```

## 快速创建（$$）

```
<script>

$$(TagName, AttrArray, ParentNode)
//常见的创建方式：
//var div=document.createElement(“div”);
//div.id=”id1”;
//div.style.display=”block”;
//div.style.backgroundColor=”#fff”;
//document.body.appendChild(div);
uform:
$$(“div”,{ “id” : “id1” , “style” : {“display” : “block” , “backgroundColor” : “#fff” }},document.body);
//简单粗暴

</script>
```

## 动画（animate）

```
<script>

$().animate(StyleArray, SpendTime)
StyleArray  如：{“left”:”100px”}
function an(){
$(".oDiv").animate({"left":"100px","filter":"alpha(opacity=100)", //IE"MozOpacity":"1", 
"KhtmlOpacity":"1", "opacity":"1"},500);
}

<style type="text/css">

html,body{width:100%; height:100%; margin:0; font-size:14px;}
.oDiv{position:absolute; font-size:18px; width:200px; height:50px; top:200px; 
filter:alpha(opacity=0); 
-moz-opacity:0; -khtml-opacity: 0; opacity: 0;}    
   </style>
        <body>
           <input onclick="an()">/>
           <div class = "oDiv">效果</div>
        </body >
   </script>
```

## Ajax\(U.A.Request\)

```
<script>
    U.A.Request("URL", (["参数"])).value;
</script>
```

## 阻止冒泡

```
<script>
    U.M.StopBubble();
</script>
```

## 获取有效元素孩子节点\(Child\)

```
<script>
    $(div).Child();

</script>
```

## 获取上级父亲层\(Parent\)

```
<script>
    $(div).Parent();
</script>
```

## 克隆元素\(clone\)

```
<script>
    $(div).clone();
</script>
```

## 添加元素到制定的位置\(appendTo\)

```
<script>
    $(div).appendTo(div2);
</script>
```

## 插入元素\(append\)

```
<script>
    $(div).append(div2);
</script>
```

## 移除元素\(remove\)

```
<script>
    $(div).remove();
</script>
```

## 移除元素\(remove\)

```
<script>
    $(div).remove();
</script>
```

## 添加innerHTML\(html\)

```
<script>
    $(div).html("");
</script>
```

## css3动画使用\(transition\)

```
<script>
    $(div).transition({scale:"1.5"});
</script>
```



