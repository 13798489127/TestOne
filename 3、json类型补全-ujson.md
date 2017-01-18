## Json类型补全U.Json

---

* ##### U.Json是本框架的一个特色，完善了对Json数据类型的操作。系统json只提供了2个函数：从字符串转换为json，从json转换为

##### 字符串，不能满足系统的需要。



> 示例数据：

       var dg = \[

{"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},

{"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},

{"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},

{"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}},

{"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}},

{"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}}

\];



图：



注：

此数据为树数据，适宜作为案例。

用法：\_$\(dg\).函数名\(参数,参数….\)

