# 对话框

---

  
使用方法：U.UI.Dialog\(c,t,id,w,h\);

参数一（c）：元素对象对话框内容

参数二（t）：str标题默认为“对话框”

参数三（id）：str窗体id

参数四（w）：int窗体宽度默认400

参数五（h）：int窗体高度默认550

示例：

                        阿斯达

var c = $$\("div"\);

$$\("h1", {"style":{ "textAlign": "center", "margin": "25px 10px 25px 10px", "max-width": "400px", }, "innerHTML": "关于云端操作系统发布手机版本公告"}, c\);

$$\("div", {"style":{ "margin":"10px", "text-indent": "2em", "font-size" : "14px" }, "innerHTML": "经过项目团队的不断努力，云端操作系统手机版将于2016年12月14日发布，网页访问网站为m.1473.cn" },c\);

U.UI.Dialog\(c\);

返回窗体：

