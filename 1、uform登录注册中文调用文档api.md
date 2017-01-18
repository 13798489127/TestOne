# UForm登录注册中文调用文档API

---

### 1、简介：

登录注册是一个基于 ufrom 的登录窗体，它能够很方便、很轻松的帮助您在网站中构建功能丰富、交互性强的登录注册，主要功能有：

```
           支持基本登录、注册。

           支持找回密码

           拥有验证码区域

           支持微博账号登录，QQ账号登录

           支持用户通过Cookie自动登录,Cookie登录入口。支持跨域

           支持登录状态中的账号重复登录顶下线提醒。
```

### 2、兼容性：

Internet Explorer 8及以上、Firefox、Chrome、Safari 、360、qq以及 Opera 支持;

### 3、使用方法

##### 3.1、引入文件

&lt;!-- 引用强大的urform.框架 帮助效率开发 地图控件的开发都是基于这个框架--&gt;

&lt;script type="text/javascript" src="[http://www.1473.cn/uform.js"&gt;&lt;/script&gt;](http://www.1473.cn/uform.js"&gt;&lt;/script&gt);

&lt;!-- 最后就是这个自己操作的js啦--&gt;

&lt;script src="U.U.L.js" type="text/javascript"&gt;&lt;/script&gt;

##### 3.2、HTML：无

### 4、调用方法

##### 4.1、U.U.L.DLTC\(UIE,UCB\){};登录注册

配置:

| 参数 | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| UIE | Int | 0 | UIE==3：登录页面，             UIE==1：注册页面，             UIE==2：找回密码页面 |
| UCB | function | undefined | 回调函数 |
| \_UDOD | 字符串 | $\("\#UD\_SYC"\) | 获取登录登录注册框 |

登录调用方法:U.U.L.DLTC\(3\)

注册调用方法:U.U.L.DLTC\(2\)

调用后返回： true  or  false

##### 4.2、登录注册切换函数

U.U.L.SDL（UTF, UCB\);

配置：

| **参数** | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| UTF | 字符串/int | 0 | UIE==3：登录页面，UIE==1：注册页面，UIE==2：找回密码页面 |
| UCB | function | undefined | 回调函数 |

注册接口：

```
U.A.Request("UseStudioManage.userregisterAjax", ([UN, UP, UE, UC, TI, ""]), cb, ([[$("body")[0], true]]));

@param UN 用户名

@param UP 用户密码

@param UE 邮箱

@param UC 省份证号

@param TI TypeID

@param

@param cb 回调函数 

@param ude 回调传参 [[load元素, true], arg, arg......]
```

示例：U.U.L.SDL\(3\);

结果：从切换到登录界面

##### 4.3、登录enter

U.U.L.ENDL \(UDOD, UDTD\)

| **参数** | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| UDOD | int | undefined | 点击元素 |
| UCB | function | undefined | 回调函数 |

##### 4.4、登录调用回调使用

U.U.L.SYDLHD\(UFN\)

| **参数** | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| UFN | Array | true | 返回登录状态 |

返回值:return true

##### 4.5、点击微博或者qq登录

U.U.L.QWDL \(UDOD, UTF\)

| **参数** | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| UDOD | Element |  | 按钮 |
| UTF | 字符串int |  | 类型判断 |

##### 4.6、Cookie登录

简介：1473.cn域下各个应用的用户通过Cookie自动登录,Cookie登录入口，支持跨域。

使用方法：U.U.L.CookieL\(\)

##### 4.7、cookie登录查看值

该函数为cookie登录的异步

函数：U.U.L.AsynCookieL\(request\);

| **参数** | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| request | object |  | 用户的云端Cookie状态 |

##### 4.8、获取用户登录cookie，

云端cookie关键字为usestudiosso，格式为

| **参数** | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| Loginid | 字符串int |  | 登录id |
| UserStamp | 字符串int |  | 账号 |
| userid | 字符串 |  | 云端用户id |
| username | 字符串int |  | 云端用户名 |

返回值: 用户登录信息

##### 4.9、1473桌面直接登录，单击登录按钮时触发的函数

U.U.L.SDLD \(UDOD, UTF\)

| **参数** | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| UDOD | Element |  | 登录所在的div元素 |
| UTF |  |  | 暂时未使用 |

##### 

##### 4.10、已经登录过的用户，执行登录回调。

U.U.L.AsynSDLD \(UDOD, UST, USE\)；

| 参数 | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| UDOD | Element |  | 登录所在的div元素 |
| UST |  |  | 暂时未使用 |
| USE | String | "登录" | 登录状态 |

##### 4.11、用户登录执行回调

U.U.L.DLHD \(\);

##### 4.12、用户登录云端接口，向后台发送请求

U.U.L.UlL \(UN, UP, UDTD, UCB\)；

| 参数 | **类型** | **默认值** | **说明** |
| :--- | :--- | :--- | :--- |
| UN | 字符串var | 0 | 用户名 |
| UP | 字符串int | 0 | 密码 |
| UDTD | Element | undefined | 登录窗口div元素 |
| UCB | function | function | 回调函数 |

返回值：请求成功返回true 否则undefined

##### 4.13、用户登录执行事件 异步

函数：U.U.L.AsynUlL\(request\)

作用：异步判断用户登录状态

##### 4.14、获取用户登录数据

函数：U.U.L.GetLogin\(UN,UCB\);

| 参数 | 类型 | 说明 |
| :--- | :--- | :--- |
| UN | string | 用户名 |
| UCB | fun | 回调函数 |

##### 4.15、异步获取数据弹出填写个人资料

U.U.L.AsynGetLogin \(request\)

##### 4.16、用户登录初始化用户资料

U.U.L.SetUserInfo \(UDE, UTF\)

| 参数 | 类型 | 说明 |
| :--- | :--- | :--- |
| UDE | Array | 用户信息 |
| UTF | Boolean | 是否修改判断 |

##### 

##### 4.17、登录成功执行事件

U.U.L.SLF  \(\)

##### 4.18、登录用户添加用户信息

U.U.L.TJYHXX\(\);

##### 4.19、用户头部头像个人信息

U.U.L.GRXX\(\);

##### 4.20、注销

U.U.L.ZXDLTP\(\);

##### 4.21、确认注销

U.U.L.QDZXDLTP \(UTF\);

| 参数 | 类型 | 说明 |
| :--- | :--- | :--- |
| UTF | Boolean | 是否清楚cookie |

##### 4.22、用户退出指定帐号 清理cookie

U.U.L.TCUL \(\)

##### 4.23、退出账户异步

U.U.L.AsynTCUL \(request\)

##### 4.24、用户下线或者给别人顶下线

U.U.L.UL \(UTF\)

| 参数 | 类型 | 说明 |
| :--- | :--- | :--- |
| UTF | Boolean | 是否为被顶下线 |

##### 4.25、外链登录填写登录信息

U.U.L.USUTJ\(UDE, UN\);

| 参数 | 类型 | 说明 |
| :--- | :--- | :--- |
| UDE | Array | 用户信息 |
| UN | String | 用户名 |

##### 4.26、把用户填写的账号密码写入数据库

U.U.L.TXZH \(UTF, UDE, UN, UP\)

| 参数 | 类型 | 说明 |
| :--- | :--- | :--- |
| UTF | Array | 是否修改账号密码 |
| UDE | String | 用户信息 |
| UN | String | 用户名 |
| UP | Int | 密码 |

##### 4.27、外链登录成功，异步修改个人信息

U.U.L.AsynTXZH \(request\)







