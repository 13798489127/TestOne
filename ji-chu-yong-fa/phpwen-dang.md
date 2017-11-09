# 概括

```
传统的PHP开发起来实在是不适合新手，不仅仅是它的语法非常的复杂，
而且它的函数在每个版本都会有些变化，所有你在每一个版本的时候都
会发现之前的有些函数会用不了，而且传统的PHP也会有一些浏览器兼容性的问题！
使用我们这个php，所有的读写数据工作都可以在存储过程中完成！
```

# 怎么使用? 调用一个必要文件!

```
（http://"地址":"端口"+"路径"/us.mysql.php）和 <script src="http://www.1473.cn/uform.js"></script>

PS:数据库为Mysql
```

## 连接数据库

```
//只需修改us.mysql.php的 @$m = new mysqli('地址', 'Name', 'pass', '数据库名称');
//然后前台再调用php文件
```

## 如何获取数据库表的数据

```
//比如一个user表，我想要所有用户的信息
//首先要在mysql里面建立一个存储过程 
select * from user //存储过程名字为SelecInfo
//前台调用这个存储过程
var _e = U.A.Request("http://127.0.0.1:8080/US.PHP/lib/us.mysql.php", (["SelecInfo"])).value;
//简单的取数据就这样完成了
```

## 前台如何传参

```
//var aa = U.A.Request("http://"地址":"端口"+"路径"/us.mysql.php", (["存储过程名称","参数一","参数二"]
)).value;
//当一个存储过程需要传参的时候，比如我们插入一条数据
//给用户表插入一个新的用户
//存储过程 名字：InsertData
BEGIN
    insert into user values(aName,aPass);
END
   aName varchar(255),aPass varchar(255)
//前台传参：
var _e = U.A.Request("http://127.0.0.1:8080/US.PHP/lib/us.mysql.php", (["InsertData","aName","aPass"]
)).value;
```



