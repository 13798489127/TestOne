# JS规范 {#js规范}

---

## 1、注册命名空间 {#1、注册命名空间}

```
为了使js符合传统编程语言java，net的编码习惯，特制定命名空间方法。

javascript没有命名空间，导致多个js文件之间没有规范的区分方法，容易重名，命名空间能解决此问题。
```

> 命名空间的使用方法如下：

**函数：NameSpace.register\(n, c, cb\)**

* 参数一\(n\)：命名空间

* 参数二\(c\)：方法集合

* 参数三\(cb\)：注册时候的回调函数

* 返回值\(\_UWE\)：生成变量

**示例：Namespace.register\("U.U.YY"\);**

![](/Image/image001.png)

示例二：//桌面应用变量

```
Namespace.register("US", [
                             "userinfo", //个人用户变量

                             "Disk", //网盘使用变量

                             "Blog", //朋友圈变量

                             "PB", //学习系统

                             "Friend", //用户好友"NLInfo" //系统访问用户信息

                   ]);
```

例：有公司名为百度，则注册名为BD的命名空间

```
Namespace.register\("BD"\);

百度有开发网盘的小组名为WP，注册BD.WP命名空间，则。

Namespace.register\("BD.WP"\)

网盘下有开发树目录的成员，则注册树木录命名空间TR

Namespace.register\("BD.WP.TR"\)

此树目录开发成员需要定义全局变量roottree，则：

BD.WP.TR.roottree=null;

此树目录开发成员需要定义函数获取根目录，则定义GetRoot：

BD.WP.TR.GetRoot=function\(\){

//内容

}
```

此命名空间能保证开发人员定义的变量和函数不会重名，适合团队开发。

## 2、命名空间规范 {#2、命名空间规范}

命名空间的注册需放在每个js文件的头部，下面列出常用的命名空间

* #### U.M全局 {#um全局}
* #### U.Blog博客 {#ublog博客}
* #### U.APB论坛 {#uapb论坛}
* #### U.Blog微博 {#ublog微博}
* #### U.DK硬盘 {#udk硬盘}
* #### U.F好友 {#uf好友}
* #### U.U用户 {#uu用户}
* #### U.P上传 {#up上传}

## 3、变量命名规范 {#3、变量命名规范}

全局变量的定义越少越好。\(定义全局变量一定要向组长申报，禁止使用input记录值\)

#### （1）、全局变量定义的案例 {#（1）、全局变量定义的案例}

```
全局变量必须是在整体起到关键作用的，全局变量必须是json格式的如果是单个变量的话请写好注释并且说明理由

  a    定义方法

      U.F.userid = null;//这个是正确的全局变量的定义

      var userid = null;//只是个错误的全局变量的定义

  b    json格式全局变量

       U.U.R.userinfo = {};

       U.U.R.Disk = {};

       U.U.R.Blog = {};

       U.U.R.Friend = {};
```

c 普通全局变量一定要详细注释

#### （2）、局部变量 {#（2）、局部变量}

```
a、局部变量的应用，请举例说明

b、功能区和非功能区不明确，下面举例说明
```

## 4、函数命名规范 {#4、函数命名规范}

.函数名的定义规范：**命名空间+函数名称**

例如：U.F.GetAllFriendsAjax=function\(\){}

## 5、 js使用技巧 {#5、-js使用技巧}

\(1\)可以给元素添加另外的属性，减少很多临时变量，同时能减少代码量，使程序更符合逻辑。

例如：document.getElementById\(“testdiv”\).aabb=”124”;则把124赋值给了aabb。

## 6、Namespace.Add的调用 {#6、namespaceadd的调用}

作用：添加命名属性

函数: Namespace.Add \(d, a\)

参数一\(d\)：所在的命名区域

参数二\(a\)：属性集

示例：Namespace.Add\("US",{"domain": "1473.cn"}\);

## 7 、1473常用全局变量 {#7-、1473常用全局变量}

> `"domain": "1473.cn", //主站点命名`
>
> `"LoginID": 0, //登录状态`
>
> `"ITID": "", //页面识别码`
>
> `"ofs": "http://office.1473.cn/usoffice/", //office打开文件对应链接`
>
> `"fs": "http://fs.1473.cn/", //fs对应的链接`
>
> `"afs": "http://appfs.1473.cn/", //站外应用链接`
>
> `"ms": "http://www.1473.cn/", //主站域名`
>
> `"ER": "http://www.1473.cn/img/error.png", //错误图片`
>
> `"PID": "1e0742d8-737e-46e2-b03b-2f23ca8c1f17", //论坛根目录id`
>
> `"OG": "d8ae0266-481d-4064-86d2-fb52a4059793", //我的电脑id`
>
> `"SG": "9639aba6-03eb-443c-be4e-f0c8d24767f5", //私密文件夹id`
>
> `"FG": "f6d7a4b6-e34c-4964-beed-24187b2cb1ba", //FTP文件夹id`
>
> `"DG": "7aeaab56-485f-4150-b781-8ffd86d593ce", //我的文件夹id`
>
> `"PG": "93553847-e299-464c-a0e2-c15872efb6ae", //图片文件夹id`
>
> `"MG": "8a2135ff-746a-43a8-97b8-552d228a00bb", //我的音乐文件夹id`
>
> `"VG": "bf21bf7a-1e95-4194-8e4a-e9334d7d998d", //视频文件夹id`
>
> `"Height": window.screen.availHeight, //页面高度`
>
> `"Width": window.screen.availWidth, //页面长度`
>
> `"NU": "00000000-0000-0000-0000-000000000000", //空id`
>
> `"ZV": 20,//页面层次`
>
> `"PB": {`
>
> ```
> "News": null, //论坛消息
>
> "YJF": "3c779543-bc1a-4851-af22-af9ba97a5f33" //意见反馈目录id
> ```
>
> `}`



