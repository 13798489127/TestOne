# UForm登录注册中文调用文档API

---

1、简介：

登录注册是一个基于 ufrom 的登录窗体，它能够很方便、很轻松的帮助您在网站中构建功能丰富、交互性强的登录注册，主要功能有：

```
           支持基本登录、注册。

           支持找回密码

           拥有验证码区域

           支持微博账号登录，QQ账号登录

           支持用户通过Cookie自动登录,Cookie登录入口。支持跨域

           支持登录状态中的账号重复登录顶下线提醒。
```

2、兼容性：

Internet Explorer 8及以上、Firefox、Chrome、Safari 、360、qq以及 Opera 支持;

3、使用方法：

3.1、引入文件：

&lt;!-- 引用强大的urform.框架 帮助效率开发 地图控件的开发都是基于这个框架--&gt;

&lt;script type="text/javascript" src="[http://www.1473.cn/uform.js"&gt;&lt;/script&gt;](http://www.1473.cn/uform.js"&gt;&lt;/script&gt);

&lt;!-- 最后就是这个自己操作的js啦--&gt;

&lt;script src="U.U.L.js" type="text/javascript"&gt;&lt;/script&gt;

3.2、HTML：无

3.3、Javasrcript\(调用方法\):

3.3.1、U.U.L.DLTC\(UIE,UCB\){};登录注册

配置:

选项    类型    默认值    说明

UIE    Int    0    UIE==3：登录页面，UIE==1：注册页面，UIE==2：找回密码页面

UCB    function    undefined    回调函数

\_UDOD    字符串    $\("\#UD\_SYC"\)    获取登录登录注册框

登录调用方法:U.U.L.DLTC\(3\)；

注册调用方法:U.U.L.DLTC\(2\)；

调用后返回： true;  or  false

3.3.2、登录注册切换专用函数

U.U.L.SDL（UTF, UCB\){};

配置:

选项    类型    默认值    说明

\_UDCD    Obj    \[\]    聚焦处理

UCB    function    undefined    回调函数

UTF    字符串/int    0    UIE==3：登录页面，UIE==1：注册页面，UIE==2：找回密码页面

\_UTF    Array    true    判断是否登录

注册接口

U.A.Request\("UseStudioManage.userregisterAjax", \(\[UN, UP, "", "", 16, ""\]\),

@param UN 用户名

```
@param UP 用户密码

    @param 邮箱

     @param 

     @param TypeID

     @param
```

例如: U.U.L.SDL（3）;从注册界面切换到登录界面

返回值: undefined

3.3.3、登录enter

U.U.L.ENDL \(UDOD, UDTD\);

选项    类型    默认值    说明

UDOD    int    undefined

UCB    function    undefined    回调函数

3.3.4、登录调用回调使用

U.U.L.SYDLHD\(UFN\)

选项    类型    默认值    说明

UFN    Array    true    返回登录状态

返回值:return true

3.3.5、点击微博或者qq登录

U.U.L.QWDL \(UDOD, UTF\)

选项    类型    默认值    说明

UTF    Array    0    选择QQ或者是微博

UDOD    字符串 int     0    点击元素判断函数

3.3.6、Cookie登录

简介：1473.cn域下各个应用的用户通过Cookie自动登录,Cookie登录入口。

支持跨域

U.U.L.CookieL\(\);

选项    类型    默认值    说明

\_UTF    字符串 int     U.U.L.GLID\(\);    获取用户的云端Cookie

\_UST    字符串 int     US.NLInfo.LogAddr \|\| "";    获取用户登录的cookie

3.3.7、cookie登录查看值

U.U.L.AsynCookieL\(request\);

选项    类型    默认值    说明

request    字符串 int         用户的云端Cookie状态

3.3.8、获取用户登录cookie，

云端cookie关键字为usestudiosso，格式为

选项    类型    默认值    说明

UID    字符串 int         用户的ID状态

Loginid    字符串 int        登录id

UserStamp    字符串 int        账号

userid

```
字符串        云端用户id
```

username    字符串 int        云端用户名

返回值: return \_UDE;//内含数组为用户登录信息

3.3.9、1473桌面直接登录，单击登录按钮时触发的函数

U.U.L.SDLD \(UDOD, UTF\)

选项    类型    默认值    说明

UDOD    字符串 var         登录元素按钮

UTF    Array    undefined    登录状态

3.3.10、已经登录过的用户，执行登录回调。

U.U.L.AsynSDLD \(UDOD, UST, USE\)；

选项    类型    默认值    说明

UDOD    字符串 var         登录框

UST    Array    undefined    登录状态

USE

3.3.11、用户登录执行回调

U.U.L.DLHD \(\);

此函数如果没有其他应用调用，则该和上一函数合并。

3.3.12、用户登录云端接口，向后台发送请求

U.U.L.UlL \(UN, UP, UDTD, UCB\)；

选项    类型    默认值    说明

UN    字符串 var     0    用户名

UP    字符串int    0    密码

UDTD    Array    undefined    登录窗口div元素

UCB    function     function    回调函数

return true;

3.3.13、用户登录执行事件

U.U.L.AsynUlL\(request, UTF\)

选项    类型    默认值    说明

request    Array    0    登录参数

UTF    Array    0    设置好友信息

return request;//登录异步

3.3.14、获取用户登录数据、

U.U.L.GetLogin\(UN\);

选项    类型    默认值    说明

UN    Array    0    用户ID

3.3.15、异步获取数据弹出填写个人资料

U.U.L.AsynGetLogin \(request\)；

选项    类型    默认值    说明

request    Array    0    用户信息

3.3.16、用户登录初始化用户资料

U.U.L.SetUserInfo \(UDE, UTF\) ；

选项    类型    默认值    说明

UDE    Array    0    用户信息

UTF    字符串int    0    用户信息数量

return US.userinfo;

3.3.17、登录成功执行事件

U.U.L.SLF  \(UIF\)；

选项    类型    默认值    说明

UIF    Array    0

3.3.18、登录用户添加用户信息

U.U.L.TJYHXX\(\);

3.3.19、用户头部头像个人信息

U.U.L.GRXX\(\);

3.3.20、注销

U.U.L.ZXDLTP（）;

3.3.21、确认注销

U.U.L.QDZXDLTP \(UTF\)；

选项    类型    默认值    说明

UTF    Array    0    传入用户ID

3.3.22、用户退出指定帐号 清理cookie

U.U.L.TCUL \(UCB\) ；

选项    类型    默认值    说明

UCB    Array    0    传入用户cookie

3.3.23、退出账户异步。

U.U.L.AsynTCUL \(request\)

选项    类型    默认值    说明

request    Array    0    账号信息

3.3.24、用户下线获取给别人顶下线

U.U.L.UL \(UTF\)；

选项    类型    默认值    说明

UTF    Array    0    状态

3.3.25、填写登录信息

U.U.L.USUTJ\(UDE, UN\);

选项    类型    默认值    说明

UDE    Array    0    登录信息

UN    Int    0    用户账号

3.3.26、把用户填写的账号密码写入数据库

U.U.L.TXZH \(UTF, UDE, UN, UP\)

选项    类型    默认值    说明

UTF    Array    0    登录密匙

UDE    Int    0    获取密匙处

UN    Int    0    账号

UP    Int    0    密码

3.3.27、外链登录成功 同时修改个人信息

U.U.L.AsynTXZH \(request\)

"Country": "中D国¨²",

```
"Province": \_USE.province \|\| "",

        "UserEmail": \_USE.UserEmail \|\| "",

        "Birthday": U.MT.getTimeStr\(\_USE.Birthday, "String"\),

        "City": \_USE.city \|\| "",

        "UserAddress": \_USE.location \|\| "",

        "UserNickName": \_USE.screen\_name \|\| \_USE.nickname,

        "UserRemarks": \_USE.description \|\| "",

        "UserIndividualitysignature": \_USE.description \|\| "",

        "UserThumbnailImageHead": \_USE.avatar\_large \|\|
```

选项    类型    默认值    说明

request    Array    0    个人信息组

Ufrom 框架获取元素方式

