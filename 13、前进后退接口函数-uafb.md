# 前进后退接口函数U.AFB

---

### 1、全局变量

```
U.AFB.GoList = {}; //前进后退处理

       U.AFB.UTH = null //url处理
```

### 2、U.AFB.RGoL

```
作用：前进后退公开调用

使用方法：U.AFB.RGoL(UTF, UFT);

参数一（UTF）：string 前进后退在指定的域

参数二（UFT）：boolean 是否重新加载  默认不重新加载

示例：U.AFB.RGoL("Disk");
```

### 3、U.AFB.init

```
作用：注册前进后退

使用方法：U.AFB.init(UTF);

参数（UTF）： string 前进后退在指定的域 如 disk 那就在disk导航
```

#### 3.1设置原型  运行实例化使用

```
U.AFB.init.prototype = {

        AddEvent: U.AFB.AddEvent,   

        AddDrawBack: U.AFB.AddDrawBack,

        GQH: U.AFB.GQH,

        DrawBack: U.AFB.DrawBack,

        GoForward: U.AFB.GoForward

}
```

### 4、U.AFB.AddEvent

```
作用：添加前进后退

使用方法：U.AFB.AddEvent(UCB, UTF)

参数一（UCB）：function 前进后退函数添加

参数二（UTF）：string   前进后退在指定的域

示例：U.AFB.AddEvent([[T.U.MU.D.ZDXX, ([_UID, _FTID, _FName, "Disk"])]], "MD");
```

### 5、U.AFB.AddDrawBack

```
作用：添加前进后退事件

使用方法：U.AFB.AddDrawBack(UCB)

参数（UCB）：function 前进后退函数添加
```

### 6、 U.AFB.GQH  未使用

```
作用：前进后退统一处理区

使用方法：U.AFB.GQH(UTF);

参数（UTF）：{number} 前进后退处理参数

----------1 前进处理

----------0 后退处理
```

### 7、U.AFB.DrawBack

```
作用：后退执行

使用方法：U.AFB.DrawBack(UTF)

参数（UTF）：string 前进后退在指定的域

示例：U.AFB.DrawBack("Disk")
```

### 8、U.AFB.GoForward

```
作用：前进执行

使用方法：U.AFB.GoForward(UTF)

参数（UTF）：string 前进后退在指定的域

示例：U.AFB.GoForward("Disk")
```

### 9、U.AFB.UHash

```
作用：添加路由监视
使用方法：U.AFB.UHash(UCB)

参数（UCB）：function 监督url hash变化的处理

返回值：obj 返回路由对象

示例--加载网盘信息：

U.Dk.DI.WPFF(true, U.M.apply(this, [[U.AFB.UHash, ([U.D.G.UrlGuide])]]));
```

### 10、U.AFB.TJ 未使用

```
作用：路由统计

使用方法：U.AFB.TJ(UDE)

参数（UDE）：Array  [0]  记录的url处理
                   [1]  回调函数
```

### 11、U.AFB.Set 未使用

```
作用：添加独立路由设置

使用方法：U.AFB.Set(UDE)

参数（UDE）: function 监督url hash变化的处理
```

### 12、U.AFB.Add 未使用

```
作用：添加设置Hash

使用方法：U.AFB.Add(UDE, UN)

参数一（UDE）：Array 用户路径

如：http://www.1473.cn/\#!/disk/13798489127/f6d7a4b6-e34c-4964-beed-24187b2cb1ba  

则：UDE = ["disk", "13798489127", "f6d7a4b6-e34c-4964-beed-24187b2cb1ba"]

参数二（UN）：str  用户名或标题  默认为 "1473.cn"
```

### 13、U.AFB.Path  未使用

```
功能：初始化url导航

使用方法：U.AFB.Path(UCB)

参数（UCB）：function回调函数 监督url hash变化的处理
```

#### 13.1 constructor 方法

* 作用：重载U.AFB.Path

#### 13.2  UHash 方法

* 作用：重载U.AFB.UHash

#### 13.3 TJ方法

* 作用：重载U.AFB.TJ

#### 13.4 Set方法

* 作业：重载U.AFB.Set

#### 13.5 Add方法

* 作用：重载U.AFB.Add

#### 13.6 init

* 作用：初始化

#### 13.6 Ch 方法

* 作用：地址变化使用

#### 13.7 setNC 方法

* 作用：设置当前使用

#### 13.8 ICH 方法

* 作用：IE处理  Hash值ie变化

#### 13.9 AddHS 方法 IE6-7支持

* 作用：设置属性

#### 13.10 ICHT方法

* 作用：IE8一下的浏览器保存记录

#### 13.11 UQJH 方法

* 作用：产生一个接收前进后退的Iframe

#### 13.12 AUQJH 方法

* 作用：前进后退回调

#### 13.13 GO方法

* 作用：前进后退执行

### 14、重载U.AFB.Path.prototype方法

            U.M.Setprototype\(U.AFB.Path.prototype.init, U.AFB.Path.prototype\);

作用：将U.AFB.Path.prototype的方法重载到U.AFB.Path.prototype.init中

