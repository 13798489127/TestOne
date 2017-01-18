# 动态加载U.MD

---

### 1、U.MD.DynamicLoad

```
功能：jsonp初始化对象

使用方法：U.MD.DynamicLoad(UURL,UTP,UCB,UDE,UTF)

参数一：string获取的地址，例如  http://cbks.baidu.com/js/m.js

参数二：string获取的类型：jscss

参数三：function回调函数

参数四：object { "src" : "http://cbks.baidu.com/js/m.js" , "type" ："text/javascript" }

参数五：boolean是否重复加载文件

返回值element对象
```



### 2、U.MD.IframeLoad

```
功能：设置异步加载文件或者iframe

使用方法：U.MD.IframeLoad(UDOD,UCB)

参数一：element加载的元素

返回值function回调函数

示例：U.MD.IframeLoad($("iframe",{"width":"100px","height":"100px"},document.body),function(){})
```



### 3、U.MD.IframeLoad.AILD\(\)

```
功能：onload成功进入

使用方法：U.MD.IframeLoad.AILD(UDOD,UCB)

参数一：element加载的元素

返回值function回调函数
```



### 4、U.MD.ISWJCZ

```
    功能:判断文件是否存在
```

### 5、U.MD.loading

```
功能：设置元素loading

使用方法：U.MD.loading(UDOD,UTF)

参数一：element元素

参数一：boolean设置loading类型

示例：U.MD.loading($("#UD_SYF_F")[0], true)
```



### 6、U.MD.loading.Donresize

```
功能：loading变化设置
    
参数一：element当前loading元素    
```



### 7、U.MD.uploading

```
功能：取消loading

使用方法：U.MD.uploading(UDOD)

参数一：element当前loading元素

示例：U.MD.uploading ($("#UD_SYNR")[0])

返回：true
```



