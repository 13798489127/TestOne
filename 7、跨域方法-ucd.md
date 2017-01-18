## 跨域方法U.CD

---

1、纯数据跨域解决办法

函数：U.CD.LIFA\(t,cb\)

参数一（t）：是否加载外链数据  默认加载Main Disk BG Pay reply

形如\[iframeName CDFilePath ajaxName\]

            iframeName iframe的名字

             CDFilePath CD.html文件的路径

             ajaxName Ajax请求的名字

参数二（cb）：回调函数

示例：加载外链数据Admin数据

U.CD.LIFA\(\[\["admin", "http://admin.1473.cn/index.htm", "AAjax"\]\], function \(\) {  console.log\(U.AAjax.Request\("ADisk.GetFileByTypeId", \(\[6, 0, 10\]\)\).value\);//获取建站diy的前10调数据   }\);

注：需要挂载到1473子域名下才可使用

2、调用窗体（UI）的跨域解决办法

注：需要引用uform.css 和 uformd.js才可使用

函数：U.CD.GQB\(t, cb\);

参数一（t）：是否加载外链数据  默认加载Main Disk BG Pay reply

形如\[iframeName CDFilePath ajaxName\]

            iframeName iframe的名字

             CDFilePath CD.html文件的路径

             ajaxName Ajax请求的名字

参数二（cb）：回调函数

示例： U.CD.GQB\(null, function \(\) {

      U.D.DT.YYDK\("Blog"\); //获取圈子窗体及数据（云盘朋友圈）

}\);

