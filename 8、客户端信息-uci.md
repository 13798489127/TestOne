# 客户端信息 U.CI

---

### 一、获取客户端信息U.CI.GCUInfo的调用

函数名: U.CI.GCUInfo\(callback\)

参数一\(callback\)：回调函数

实例: U.CI.GCUInfo\(function\(\){}\);

### 二、获取客户端ip异步U.CI.AsyGCUInfo的调用

函数名: U.CI.AsyGCUInfo\(callback\)

参数一\(callback\(msg\)\)：回调函数

回调函数参数

\(msg\): ip地址信息

-------country国家

-------province省

-------city城市

-------district区

实例: U.CI.AsyGCUInfo\(function\(msg\){

Console.log\(msg\);//打印信息

}\);

### 三、获取浏览器类型U.CI.getBrowser的调用

函数名: U.CI.getBrowser\(\)

无参数

返回值 {object}浏览器类型

---------browser浏览器类型如ie chrome firefox safir

---------ver浏览器版本如果ie的7.0 8.0和chrome 33 34

实例:

### 四、获取用户电脑系统U.CI.getSystem的调用

函数名: U.CI.getSystem\(\)

无参数

返回值{String}操作系统名称

实例:

### 五、判断用户支持html5还是flash U.CI.IsHF的调用

函数名: U.CI.IsHF\(\)

无参数

返回值{String} ‘html5’或’Flash’

实例:

### 六、获取浏览器信息U.CI.Browser的调用

函数名U.CI.Browser\(\)

无参数

返回值{object}浏览器信息

实例:



