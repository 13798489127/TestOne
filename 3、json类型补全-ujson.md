## [Json类型补全U.Json](/api.1473.cn/example/json.htm)

---

* ##### U.Json是本框架的一个特色，完善了对Json数据类型的操作。系统json只提供了2个函数：从字符串转换为json，从json转换为

##### 字符串，不能满足系统的需要。

> 示例数据：

```
var dg = [

   {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},

   {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},

   {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},

   {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}},

   {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}},

   {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}}

];
```

> 图：

![](/assets/image073.png)

> 注：

* 此数据为树数据，适宜作为案例。

* 用法：\_$\(dg\).函数名\(参数,参数….\)

### 3.1 Clone\(\)

```
功能：克隆对象

示例：_$( dg).Clone()

结果：
[

    {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},

    {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},

    {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},

    {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}},

    {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}},

    {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}}

]
```

### 3.2 Add\(u\)（有错）

```
功能：向json数组中添加记录。

参数一：是另外一个json。

示例：var u = {"id":"7","parentid":"0","name":"E盘","info":{"files":"111","t":"f"}};

var c =_$(dg).Add(u);

结果：

c=[

    {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},

    {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},

    {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}}, 

    {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"} },

    {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"} },

    {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"} },

    {"id":"7","parentid":"0","name":"E盘","info":{"files":"111","t":"f"}}

]
```

### 3. 3 IFOBJ\(f\)

```
功能：判断f是否为数组，f为数组，返回"Array"，否则，返回true。

参数一：数组或者Object

示例：_$().IFOBJ(dg[0])

结果：truedg[0]为json。

示例：_$().IFOBJ(dg)

结果："Array"dg为数组
```

### 3.4 count\(\)

```
功能：返回json的长度

示例：_$(dg).count();

结果：6
```

### 3.5 FindOne\(f,y\)

```
功能：查找符合条件的一个元素

参数一（f）：obj待查找的值

参数二：是否递归查找，默认值为true，传递true为递归，如传递递归节点名，速度更快。

示例：var a=_$(dg).FindOne({ "parentid": "0" })

结果：

{"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}}

注：出现结果有多条，只取第一条
```

### 3.6 sort\(s\)

```
功能：排序函数

参数一：排序键名

数据：var dg =[

                {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}}, 

                {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}}, 

                {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}}, 

                {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},

                {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}}, 

                {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}}

             ];

示例：_$(dg).sort("parentid");根据parentid进行升序排序。

结果：var dg =[

                {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}},

                {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},

                {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},

                {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},

                {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}},

                {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}},

              ];
```

### 3.7 groupBy\(u\)

```
功能：分组输出

参数一：键名

示例：_$(dg).groupBy("parentid");

结果：{
          "0":[
                {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},

                {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}}
              ],

          "1":[
                {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}} 
              ],

          "2":[              
               {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}}             
              ],

          "3":[ 
               {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}}
              ],

          "4":[
                {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}}
              ]
     }
```

### 3.8 pluck\(l,u\)

```
功能：获取指定键的值

参数一：键名

参数二：数组如果该处传参有值则查找范围为参数二所定义的范围。此时可以写成_$().pluck(l,u);

示例：

    var a=_$(dg).pluck("id");

结果：

    ["1", "2", "3", "4", "5", "6"]
```

### 3.9 Where\(u,t\)

```
功能：条件选择

参数一：
    可选值：$or   or使用
        $e    =
        $ne   !=
        lt    <
        $lte   <=
        $gt      >
        $gte   >=
        $in    in
        $nin    not in
        $all    匹配所有
        $exists    存在文档
        $mod   取模函数
        $not    不匹配

参数二：条件值

数据：var dg = [
            {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},
            {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},
            {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},
            {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}},
            {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}}, 
            {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}},
            {"id":"7","parentid":"6","name":"计算机","info":{"files":"200","t":"f"}}
           ];
示例一：_$(dg).Where({ "$e": {"name" : "计算机" }}); 匹配name为计算机的全部数据

结果：[
    {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},
    {"id":"7","parentid":"6","name":"计算机","info":{"files":"200","t":"f"}}
     ]

示例二：_$(dg).Where({ "$ne": {"name" : "计算机" }}); 匹配name为不为计算机的全部数据

结果：[
    {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},
    {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},
    {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}},
    {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}},
    {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}}
      ]
```

### 3.10 Select\(f,y,t\)

```
功能：条件搜索

参数一：搜索条件，形如{"id":"1"}的数据，非树json可以忽略后面2个参数。

参数二：是否跨越层次，true跨层，false不跨。如果传递树关键字，比如：父亲id(parentid)，则会通过关键字跨层次。可以不填.

参数三：选取多少条数据，可以不填，默认符合条件的全部数据。

示例：var a=_$(dg). Select ( { "parentid " :"0" } );

结果：a = [
            {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},
            {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"} }
          ]

注：Select是多选，选取第一条可以用FindOne函数或者用a[0]表达。
```

### 3.11 Change\(v,k\)

```
功能：修改json中的值。

参数一：修改的值，可以是集合对象、json、数组（数组中包含集合）

参数二：被修改对象，可以是集合对象、json、数组（数组中包含集合）,此时可以写成_$(). Change(修改的值，被修改对象);

示例一：_$(dg[0]).Change({ "name": "我的计算机"});

结果：此句把"计算机"改成了"我的计算机"。

示例二：_$().Change({ "name": "我的计算机"}, {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}});

结果：此句把传参二中的name键改成了"我的计算机"。
```

### 3.12 Delete\(f\)

```
功能：删除json节点，可递归删除

参数一：待删除节点的属性值。

示例一：_$(dg).Delete({"id":"4"});

结果：[
        {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},
        {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},
        {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},
        {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"} },
        {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"} },
      ]

例二：_$(dg).Delete({"name":"C盘"})

结果：[
        {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},
        {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},
        {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"} },
        {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"} },
        {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"} },
      ]
```

### 3.13 RecurD\(d,k,u\)

```
功能：递归查找,可向上查找所有父亲节点，向下找所有孩子节点。

参数一：d为保留关键字，传递null。

参数二：待查找的节点,如为父亲节点，则查找所有孩子，如为孩子节点，则查找所有父亲.

参数三：父亲节点字段名或者孩子节点字段名。

示例数据为经典的树结构，需要递归选取数据。

找孩子示例：查找"C盘"的所有子节点语句如下：

    _$(dg).RecurD(null, { "parentid": "1" }, "id");

    结果：C盘、Windows、system32、drivers。

查找Windows目录下面的所有文件夹语句如下：

    _$(dg).RecurD(null, { "parentid": "2" }, "id");

    结果：Windows,system32,drivers。

找父亲示例：查找"system32"的所有父亲

    _$(dg).RecurD(null, { "id": "3" }, "parentid");

    结果：计算机、C盘、Windows、system32。

查找"Windows"的所有父亲

    _$(dg).RecurD(null, { "id": "2" }, "parentid");

    结果：计算机、C盘、Windows
```

### 3.14 NL\(p,v\)

```
功能：只选取需要的属性

参数一（）参数二：

示例：var ar={"id":"1","name":"zs","age":"12","math":"60","chinese":"100"}

如前端只需要姓名和年龄，则定义数组：

    var sz = ["name", "age"];

    _$().NL(ar,sz);

    结果：{"name":"zs","age":"12"}。

注：相当与SQL中的select函数。

暂时无法运行
```

### 3.15 Reset\(f\)

```
功能：条件排序，等于某个值会排在前面

参数一：object

示例：_$(dg).Reset({ "name": "C盘" })

结果：[
        {"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},
        {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},
        {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},
        {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}},
        {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}},
        {"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}}
      ];

注：符合条件的将排在前面，这样可以把用户经常使用的选项提到最前面。
```

### 3.16 Like\(a\)

```
功能：模糊搜索

参数一：object

示例一：_$(dg).Like({ "name": "C" })

结果：[{"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}]

示例二：_$(dg).Like({ "name": "s" })

结果：[
        {"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},
        {"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"} },
        {"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"} },
     ]

注：凡是"name"中带"s"的都会被搜索到。
```

### 3.17 GZDL\(u\)

```
功能：选择指定字段的值

参数一：形如：["id"]

数据：var bj= {
                "好友":[1,2,3] ,
                "亲人":[4,5,6]
             };

示例：_$(bj).GZDL(["好友"])

结果：{ "好友" : [1,2,3] }

注：在分组中比较有用
```

### 3.18 IsTF\(u\)

```
功能：判断对象或者集合是否匹配

参数一：被断对象或者集合

示例一：_$(dg[0]).IsTF(dg[0])

    结果：true

示例二：_$(dg[0]).IsTF(dg[1])

    结果：false

示例三：_$(dg).IsTF(dg)

    结果：true
```

### 3.19 Merger\(\)

```
功能：拆分合并数组

示例一：_$( {"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}}).Merger()

    结果:["1","0","计算机",{"files":"100","t":"f"}]

示例二：_$().Merger("abcdefg")

    结果：["a", "b", "c", "d", "e", "f", "g"]
```

### 3.20 ToString\(\)

```
功能：把json对象转换为字符串

示例：_$(dg).ToString();

结果："[{"id":"1","parentid":"0","name":"计算机","info":{"files":"100","t":"f"}},{"id":"2","parentid":"1","name":"C盘","info":{"files":"80","t":"f"}},{"id":"3","parentid":"2","name":"Windows","info":{"files":"60","t":"f"}},{"id":"4","parentid":"3","name":"system32","info":{"files":"40","t":"f"}},{"id":"5","parentid":"4","name":"drivers","info":{"files":"20","t":"f"}},{"id":"6","parentid":"0","name":"D盘","info":{"files":"200","t":"f"}}]"

注：结果为字符串。
```



