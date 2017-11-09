# Mysql存储过程

```
//数据表
m_id                                           m_context                  m_user
cbcc45aa-fee1-11e4-ae98-00ff4a38c826         被修改过的数据                用户
f5c86f9f-fee1-11e4-ae98-00ff4a38c826         被修改过的数据                用户
f63431f2-fee1-11e4-ae98-00ff4a38c826         被修改过的数据                用户
f68c1947-fee1-11e4-ae98-00ff4a38c826         被修改过的数据                用户
f6d0a655-fee1-11e4-ae98-00ff4a38c826         被修改过的数据                用户
f7187af8-fee1-11e4-ae98-00ff4a38c826         被修改过的数据                用户
```

## 存储过程用法

```
//查询
BEGIN
#存储过程 查询数据
select m_context as '发言内容',m_user as '发言人'from f_message where m_user=arr1 order by m_id desc;
END
//定义参数
arr1 text


//删除
BEGIN
    #存储过程 删除数据
    delete from f_message where m_user=arr1;
END
//定义参数
arr1 text


//添加
BEGIN
    #存储过程 插入数据
    insert into f_message (m_id,m_context,m_user) values(uuid(),arr1,arr2);
END
//定义参数
arr1 text,arr2 text


//修改
BEGIN
    #存储过程 修改数据
    update f_message set m_context=arr1 where m_user=arr2;
END
//定义参数
arr1 text,arr2 text
```

# 概括

```
随着技术的发展，我们发现SQL Server使用起来并非那么方便，操作也是非常的
复杂。只能运行在微软的windows平台，没有丝毫的开放性可言！可伸缩性，并行
性。并行实施和共存模型并不成熟，很难处理日益增多的用户数和数据卷，伸缩性
有限，性能稳定性。SQLServer当用户连接多时性能会变的很差，并且不够稳定。
所以我们现在改用Mysql！
```

# 怎么使用？

```
//要是使用数据库肯定是要先把数据库连接上
主机地址：127.0.0.1（这个是本机的地址）//如果想要连接别人的就把别人的IP输入
用户名：root //一般都是Root，注意自己安装的时候输入安装的用户名是什么
密码：123456 //安装的时候自己设定（都要非常注意，忘记了找回会很麻烦）
```

## 创建数据库

```
//第一个需要给数据库名称这个不是说了
//第二个就是字符集了，我们web上面的是UTF-8
字符集：UTF-8 Unicode
排序规律：ufe8_general_ci
//这样一个数据库就创建好了
```

## 创建表

```
//名称ID------类型---------长度--------小数点--------不是null------主键
   Id        int             14        （空）          √           是
   user      vchar          255        （空）          √           不是
   pass      vchar          255        （空）          √           不是
//一个简单的表就这样建立好了
```

## sql语句

```
//插入语句
insert into 表("列的名字1","列的名字2") values(a,b);
// #  a 是对应列的名字1 ，  b是对应列的名字2

//查询语句
select * from 表( 获取所有数据)
select 列名  from 表 where  表.列名 = a(获取一个)
// # a 是参数

//修改语句
update * 表 set 表.列名 = a  where 表.列名 = b(修改什么值，这里一定要加where)

//删除语句
delete from 表 ;(删除所有)
delete from 表 where 表.列名 = a (删除参数)
```

## JS更换数据库Host

```
U.CD.AjaxUrl = 'http://nodejs.1473.cn/'; //默认请求页面
U.CD.AjaxCross = "http://nodejs.1473.cn/CD.htm";
U.CD.Host = "192.168.100.61"; //需要更换数据库host，在这里更换
U.CD.Database = "UseStudio_CityS"; //需要更换数据库名字，在这里更换
U.CD.LIFA([["U_ACD", "http://nodejs.1473.cn/CD.htm", "ACD"]], U.CD.AsynJWH); //初始化跨域
```



