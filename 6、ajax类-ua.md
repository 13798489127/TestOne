## ajax类  U.A

---

* 由于web开发已经从后台语言、前台hmtl混写的阶段进化到了前后台严格分离的阶段，此处只提供前后台严格分离的方法，当然，混写后台、html、ajax也是适用的。

### 1、一些内部的全局变量

#### 1.1 U.A.ASet

```
作用：所有请求的ajax对象 

类型：array
```

#### 1.2 U.A.DataBase

```
作用：数据库绑定

U.A.DataBase = {
    Reply: ["Mysql", "UseStudio_Reply"], //回复系统
    Money: ["Mysql", "UseStudio_Pay"], //交易系统
    Develop: ["Mysql", "UseStudio_Develop"] //在线编程平台
};
```

#### 1.3 U.A.Reverse

```
作用：1473对应的后台地址集

U.A.Reverse = {
    office: "http://main.1473.cn/Mian.ashx", //office
    Upload: "http://disk.1473.cn/USupfile.ashx", //上传
    UseStudioManage: "http://main.1473.cn/Mian.ashx", //main
    UseStudioDisk: "http://disk.1473.cn/UseStudiodisk.ashx", //disk
    pb: "http://pb.1473.cn/publicblog.ashx", //学习系统
    Application: "http://app.1473.cn/application.ashx", //站外应用
    Blog: "http://bmain.1473.cn/blog.ashx", //blog
    UseStudioPay: "http://pay.1473.cn/UseStudioPay.ashx", //交易
    Reply: "http://reply.1473.cn", //回复
    AApp: "http://admin.1473.cn/Application/AApp.ashx", //application
    ABlog: "http://admin.1473.cn/APB/APB.ashx", //admin blog
    APB: "http://admin.1473.cn/APB/APB.ashx", //admin pb
    AUser: "http://admin.1473.cn/User/Users.ashx", //admin user
    Verify: "http://admin.1473.cn/Verify", //admin 虚拟币
    Admin: "http://admin.1473.cn/Admin/Admin.ashx", //admin 自带后台
    ADisk: "http://admin.1473.cn/Disk/ADisk.ashx", //admindisk
    KF: "http://admin.1473.cn/system/KF.ashx" //admin 统计
}
```

### 2、U.A.Request\|\|$.ajaxAjax请求后台数据的方法

```
作用：Ajax 请求

使用方法：U.A.Request(addr, cs, cb, cbcs);

参数一（addr）：string    访问的地址

参数二（cs）：array       服务器传参

参数三（cb）：function    回调函数

参数四（cbcs）：array     函数传参 -- 这里的传参第一个为loading元素

返回值：object            ajax对象

示例： var _json = U.A.Request("http://127.0.0.1:8080/us.mysql.php", (["db", "selecttype", "本科"]), function(a){

                      //a.context保存了前端传递的参数。

                      //a.value保存了后端传递的参数。

           },(["a","b"]))。

结果：发送请求到http://127.0.0.1:8080/us.mysql.php，并向这个地址传递三个参数(数组"db", "selecttype", "本科")

注：返回值为json对象，保存在变量_json中。


其他语言示例：
       加载PHP后台的代码：          
           var _json = U.A.Request("http://127.0.0.1:8080/us.mysql.php", (["SelecInfo"])).value;
           注：此例传递了1个参数

       加载Java后台的代码： 
           var _json = U.A.Request("http://localhost:1108/USJavaServlet", (["db","selecttype","本科"])).value;
           注：此例传递了3个参数

       加载nodejs的后台代码：
           var _json=U.A.Request("http:// localhost:1337/", (["zs", "SelectAll", 1]));
           注：此例传递了3个参数

       加载net的后台方法：
           var _json=U.A.Request("http:// localhost:80/a.ashx", (["zs", "SelectAll", 1]));
           注：此例传递了3个参数
```

#### 6.2.1、方法解释

        asdadsa



