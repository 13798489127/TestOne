## 云端url指引

---

### 1、云端url的介绍

##### \(一\)url指引的定义

在web中我们所有的访问方式都是用url的方式去访问网站，而url指引的方式由下面三个部分组成：

* 域名：www.1473.cn/\#!/

* 类型：www.1473.cn/\#!/disk

* 传参：www.1473.cn/\#!/disk/userid/userdirid

##### \(二\)url的使用说明

* 调用的js文件U.D.G.js

* 对应的url触发函数U.D.G.UrlGuide

* 对应的逻辑处理函数TDHJH这个函数处理了包含功能处理流程里的功能，功能定义如下：

```
type定义：
           网盘（disk）

           好友（Friend）
```

### 2、前端url指引处理

##### \(一\)网盘处理流程

```
1.文件处理

    1)在YDHJH函数中选择了disk类型的处理

    2)disk类型调用了云盘打开函数

    3)云盘打开的流程中我们第一个参数为那个用户的UserId，第二个参数为目录或者文件id

    4)调用了U.D.DT.YYDK桌面打开函数传入disk、用户id和目录id

    5)调用了disk打开文件处理U.Dk.LE.DXWPDY函数，这里直接指定到指定的文件获取文件的内容打开打开了文件
```

```
2.文件夹处理

    1)在YDHJH函数中选择了disk类型的处理

    2)disk类型调用了云盘打开函数

    3)云盘打开的流程中我们第一个参数为那个用户的UserId，第二个参数为目录或者文件id

    4)调用了U.D.DT.YYDK桌面打开函数传入disk、用户id和目录id

    5)调用了disk打开文件处理U.Dk.LE.DXWPDY函数里面的else里面有打开文件夹的处理
```

##### \(二\)好友的处理流程

```
1.打开好友处理

    1)在YDHJH函数中选择了Friend类型的处理

    2)Firend类型调用了云盘打开函数

    3)调用了U.D.DT.YYDK打开好友应用处理

    4)调用了好友应用函数里的U.F.W.SLHCK处理好友
```

##### \(三\)登录的处理流程

```
1.弹出登录

    1)在YDHJH函数中选择了login类型的处理

    2)调用了U.U.L.DLTC好友登录弹框函数
```

```
2.弹出注册

    1)在YDHJH函数中选择了login类型的处理

    2)调用了U.U.L.DLTC好友注册弹框函数
```

##### \(四\)论坛的处理流程

```
1.弹出指定的论坛处理

    1)在YDHJH函数中选择了login类型的处理

    2)调用了U.U.L.DLTC弹出论坛应用处理

    3)在应用函数里调用了U.D.PB.CTBK处理弹出了论坛窗体
```

##### \(五\)论坛帖子处理流程

```
1.查看论坛帖子处理

    1)在YDHJH函数中选择了pbt类型的处理

    2)调用U.D.PB.A.WAPMHBK弹出帖子处理
```

##### \(六\)学习系统网盘流程

```
1.弹出学习系统云盘处理

    1)在YDHJH函数中选择了disk类型的处理

    2)disk类型调用了云盘打开函数

    3)云盘打开的流程中我们第一个参数为那个用户的UserId，第二个参数为目录或者文件id

    4)调用了U.D.DT.YYDK桌面打开函数传入disk、用户id和目录id

    5)调用了disk打开文件处理U.Dk.LTWP函数，打开指定的文件夹
```

##### \(七\)Word处理流程

```
1.Word打开到指定的文件处理

    1)在YDHJH函数中选择了word类型的处理

    2)word类型调用了word打开处理

    3)调用了U.D.DT.YYDK打开word调用

    4)调用了word应用函数里的U.D.Office.Word打开了word应用
```

##### \(八\)Excel处理流程

```
1.Excel打开到指定文件处理

    1)在YDHJH函数中选择了excel类型的处理

    2)excel类型调用了excel打开处理

    3)调用了U.D.DT.YYDK打开excel调用

    4)调用了excel应用函数里的U.D.Office.Excel打开了excel应用
```

##### \(九\)评论处理流程

```
1.弹出论坛指定的评论

    1)在YDHJH函数中选择了TZ类型的处理

    2)调用U.D.PB.A.WAPMHBK弹出帖子处理，同时传入了评论的id，这样可以直接定位到评论区域
```

##### \(十\)新消息查看流程

```
1.好友消息

    1)在YDHJH函数中选择了0类型的处理

    2)函数中调用了U.F.W.SLHCK打开好友消息查看处理

    2.通知消息

    3)在YDHJH函数中选择了1类型的处理

    4)函数中调用了id为UD_SYSSRXOA这个元素执行onclick事件处理
```

### 3、云端url指引

\(一\)后台url重写流程

1.Nginx处理模块的定义

1\)url重写模块首先会尽快nginx进行判断，在这里我们分成两种url的形式作为分配管理

2\)guid.1473.cn文件id.1473.cn直接定位到disk的一般处理文件rew.ashx中

3\)从10000.1473.cn开始编号通过nginx识别除了我们已知的域名以外的所有的域名进行处理nginx对应的文件/etc/nginx/sites-enabled/default 30-41 160-171行中

2.一般处理模块的方法处理

1\)一般处理文件对应的文件为disk.1473.cn/rew.ashx

2\)处理文件中分为两种处理的方式：

a\)office文件的处理\(office文件包含了uw,ue,pdf,rtf,mht,doc,docx,xls,xlsx,ppt,pptx\)等文件格式

b\)普通文件的处理，除了上述的文件以外所有文件都以输出文件的形式处理

### 4、云端url流程图

脑图链接地址：[http://naotu.baidu.com/file/82ee2e8f4a6f02b6b448ea6102b4150e?token=ae7057b1b27cf73b&qq-pf-to=pcqq.group](http://naotu.baidu.com/file/82ee2e8f4a6f02b6b448ea6102b4150e?token=ae7057b1b27cf73b&qq-pf-to=pcqq.group)

