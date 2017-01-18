# Confirm窗体的调用      U.UI.Confirm

---

#### 方法一：U.UI.Confirm \(C, BF, NF\);参数为三个

功能:创建一个简单的Confirm

参数一（C）：str对话框里面的内容（只能为文字）

参数二（BF）：array单击确认的回调函数，形如\[函数的名字,\(\[参数一，参数二…\]\)\]

参数三（NF）：array单击取消的回调函数，形如\[函数的名字,\(\[参数一，参数二…\]\)\]

                      示例\(文字，确认，取消\)：

确认函数：U.Que = function \(q\) { alert\(q + "窗体的确认函数"\) };

取消函数：U.Qu = function \(q\) { alert\(q + "窗体的取消函数"\)};

U.UI.Confirm \(“测试”,\[ U.Que,\(\[ "测试"\]\)\],\[ U.Qu,\(\[ "测试"\]\)\]\);

结果：弹出如下提示。当单击确认时，调用U.Que，单击取消时，调用U.Qu。



#### 方法二：U.UI.Confirm\(T,S,QF,BF,C,SO\);参数为六个

功能：创建一个自定义属性的Confirm

参数一（T）：str标题

参数二（S）：{obj}对话框样式

参数三（QF）：fun单击取消的回调函数形如U.M.apply\(null, \[\[函数的名字,\(\[参数一，参数二…\]\)\]\]\);

参数四（BF）：fun单击确认的回调函数形如U.M.apply\(null, \[\[函数的名字,\(\[参数一，参数二…\]\)\]\]\);

参数五（C）：str对话框内容添加至内容区域的元素如$\("\#test"\)\[0\]

参数六（SO）：暂无作用

示例（输入文本框，确认，取消）：

         确认函数：

U.Test = function \(r,l\) {

//r保存了第一个input。

//l保存了第二个input。

}

var \_UFFD = $$\("div", {"style": {"text-align" : "center"}, "id":"test" }\); //创建对话框中的内容div元素。

$$\("span", { "innerHTML": "请输入行数：" }, \_UFFD\); //追加字符串

var \_h = $$\("input", {}, \_UFFD\); //追加输入框

$$\("div", {}, \_UFFD\);//追加div用于换行

$$\("span", { "innerHTML": "请输入列数：" }, \_UFFD\); //追加字符串

var \_l = $$\("input", {}, \_UFFD\); //追加输入框

var \_CUM = new U.UI. Confirm \("创建表格Table", { "width" : "350px", "text-align" : "center" }, null, U.M.apply\(null,\[\[U.Test,\(\[\_h ,\_l\]\) \]\]\),\_UFFD\); //创建对话框



结果：弹出如下提示。当单击确认时，调用U.Test，单击取消时，调用U.Qu。

注：如需做取消回调，修改null参数为函数即可。

