# 本地存储U.DW

---

1、U.DW.local

```
作用：异步加载跨域

使用方法：U.DW.local (UTP, UDE)

参数一（UTP）：boolean  是否存储永不过期

参数二（）：object  储传参对象

返回值：object  本地存储使用对象

```



2、U.DW.local.init

```
作用：初始化本地存储查看

使用方法：U.DW.local.init(UTP, UDE)

参数一（UTP）：boolean  是否存储永不过期

参数二（）：object  储传参对象

返回值：object  本地存储使用对象
```



3、U.DW.local.\_cb

```
作用：兼容storage事件触发 ie8-

使用方法：U.DW.local._cb (UTH)

参数： object    U.DW.local实例对象
```



4、U.DW.local.iep

```
作用：ie兼容属性设置

使用方法： U.DW.local.iep(UTH, UE)

参数一（UTH）： U.DW.local实例对象

参数二（UE）：storage事件

返回值：storage事件
```



5、U.DW.local.get

```
作用：ie获取变化内容

使用方法：U.DW.local.get(UTH)

参数：object U.DW.local实例对象

返回值：object event值
```



6、U.DW.local.init.prototype

作用：添加方法

6.1 on方法

```
作用：事件绑定

使用方法：this.on(UDE)

参数：object U.DW.local实例对象

示例：this.on(UDE.event)
```



6.2 off方法

```
作用：取消时间绑定

示例：this.off();
```



6.3 set方法

```
作用：设置值

使用方法：this.set (UDE, USE)

参数一（UDE）：object需要存储的值 如  {id:"aaa"}

参数二（USE）：string 值   当这个参数存在的使用 参数一是 string的key 这个参数为值
```



6.4、storage方法

```
作用：storage事件回调

使用方法：this.storage(ue)

参数：number U.DW.local实例对象
```



6.5、get方法

```
作用：事件绑定

使用方法：this.get(uie)

参数：number U.DW.local实例对象
```

6.6、getAll方法

```
作用：获取所有的值

使用方法：this.getAll()

返回值：obj  值的对象
```



6.7、getAllKey方法

```
作用：获取所有的键

使用方法：this.getAll()

返回值：obj 键的对象
```

6.8、remove方法

```
作用：移除值

使用方法：this.remove(UIE)

参数：string 、 object 移除的键值

返回值：object 本地存储类
```



6.9、clear方法

```
作用：移除所有的存储

使用方法：this.clear()
```



6.10、key方法

```
作用：索引值

使用方法：this. key(ui)

参数：string 键值

返回值：string 键值对应值
```



6.11、length方法

```
作用：获取长度

使用方法：this.length()

返回值：number 长度
```



