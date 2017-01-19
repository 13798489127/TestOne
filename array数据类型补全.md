# Array数据类型补全

---

#### 2.3.1 Array.isArray\(\)

```
功能：判断是否是数组类型

参数一：任何类型的变量

返回值：true或者false

示例：Array.isArray([1,2,]);

      Array.isArray(“string”);

结果：true

      False
```

#### 2.3.2 Array.from\(\)

```
功能：将string变量转换成数组

参数一：string变量

返回值：数组

示例：Array.from(‘string’)

结果：["s", "t", "r", "i", "n", "g"]
```

#### 2.3.3 Array.of\(\)

```
功能：将arguments对象转换成对象

参数：变量

返回值：该变量的类型

示例：Array.of({a:'a'})

结果：[Object]
```

#### 2.3.4 Arrayobj.inArray\(\)

```
功能：判断数组里是否like指定值

参数：整型或字符串类型

返回值：返回该值在数组的下标

示例：[1,2].inArray(1)

结果：0
```

#### 2.3.5Arrayobj.unique\(\)

```
功能：移除数组里相同的值

    暂无相关解释
```

#### 2.3.6 Arrayobj.forEach\(\)

```
功能：遍历数组

参数：回调函数

返回值：undefined

示例：[1,2].forEach(function(i){console.log(i)})

结果：12
```

#### 2.3.7 Arrayobj.every\(\)

```
功能：判断该数组中的元素值是否通过条件

参数：return条件的回调函数

返回值：true或者false

示例：[2,4,321,321].every(function(i){return i>1})

结果：true
```

#### 2.3.8 Arrayobj.some\(fun\)

```
功能：匹配一项

参数：匹配函数

返回值：最终结果

示例：var ages = [32, 33, 16, 40];

     ages.some(function (i) { return i > 18;})

返回值：true
```

#### 2.3.9 Arrayobj.map\(\)

```
功能：匹配每项

参数：匹配函数

返回值：每项匹配结果

示例： var ages = [32, 33, 16, 40];

      ages.map(function (i) { return i > 18;})

返回值：[true, true, false, true]
```

#### 2.3.10 Arrayobj. Filter\(\)

```
功能：判断该数组中的元素质是否通过条件并生成新数组

参数：return条件的回调函数

返回值：一个新的数组

示例：[2,4,321,321].filter(function(i){return i>100})

结果：[321, 321]
```

#### 2.3.11 Arrayobj.reject\(\)

```
功能：传递给失败回调函数的可选的参数

暂无相关解释
```

#### 2.3.12 Arrayobj.indexOf\(\)

```
功能：索引数组中的值

参数：整型或string类型

返回值：数组中相应值的下标或-1

示例：[1,2].indexOf(2)

结果：1
```

#### 2.3.13Arrayobj.findIndex\(\)

```
功能：返回一个指标满足提供的功能数组中的第一个元素的下标值否则返回-1

参数：return条件的回调函数

返回值：满足条件的第一个元素的下标 否则返回-1

示例：[1,2].findIndex(function(i){return i>1})

结果：1
```

#### 2.3.14 Arrayobj.includes\(\)

```
功能：判断当前数组是否包含指定的值如果是返回true否则false

参数一：需要查找的元素值

参数二：索引值，默认为0

返回值：boolean类型值

示例：[1,2].includes(1)

结果：true
```

#### 2.3.15 Arrayobj.lastIndexOf\(\)有功能相似的函数

```
功能：返回指定的值在数组中的最后一个匹配项的索引。

参数一：必需 要在Arrayobj中定位的值

参数二：可选 索引值

返回值：数组中最后一个匹配项的索引 如未找到返回-1

示例：[1,2].lastIndexOf(1)

结果：0
```

#### 2.3.16Arrayobj.reduce\(\)

```
功能：接收一个函数作为累加器，数组中的每一个值开始缩减，最终为一个值。排序为升序

参数一：回调函数包含4个参数

       1.上一次调用回调函数返回的值，或是提供的初始值

       2.数组中当前被处理的元素

       3.当前被处理元素在数组中的索引

       4.调用reduce方法的数组

参数二：可选 作为第一次调用回调函数的第一个参数

返回值：最后一次调用回调函数返回的结果

示例：[1,2].reduce(function(a,b,c,d){console.log(a,b,c,d)})

结果：1 2 1 [1, 2]
```

#### 2.3.17 Arrayobj.reduceRight\(\)

```
功能：应用一个函数针对数组的两个值，为其减至一个值。排序为降序

参数一：回调函数包含4个参数

       1.上一次调用回调函数返回的值，或是提供的初始值

       2.数组中当前被处理的元素

       3.当前被处理元素在数组中的索引

       4.调用reduce方法的数组

参数二：作为第一个参数回调的第一次调用使用

返回值：返回数组reduceRight的单一值

示例：[1,2].reduceRight(function(a,b,c,d){console.log(a,b,c,d)})

结果：2 1 0 [1, 2]
```

#### 2.3.18 Arrayobj.sample\(\)

```
暂无相关解释
```

#### 2.3.19 Arrayobj.fill\(\)

```
功能：填充所有从一开始的索引数组结束索引使用静态值的元素

参数一：任意变量

参数二：开始

参数三：结束

返回值：修改后的数组

示例：[1,2].fill(5)

结果：[5,5]
```

#### 3.3.20 Arrayobj.copyWithin\(\)

```
功能：拷贝数组的部分并返回。

参数一：目标 （下标）

参数二：开始

参数三：结束

返回值：一个完成功能后产生的一个新数组

示例：[1,2,3,4,5].copyWithin(1,0,1)

结果：[1, 1, 3, 4, 5]
```

#### 2.3.21 Arrayobj.toSourse\(\)

```
功能：返回对象的源代码

参数一：无参

返回值：返回以json形式显示数组的源代码

示例：[]

注：该函数暂时无法使用
```

#### 2.3.22 Arrayobj.keys\(\)

```
功能:数组迭代

参数一：无参
```

#### 2.3.23 Arrayobj.entries\(\)

```
功能：返回一个新数组 包含数组对象中每一个索引的键值

参数：无参

返回值：一个新Array对象

示例：var a = [a,b].entries()

     a.next().value

     a.next().value

结果：[0, a]

     [1, b]
```

---

[Array数据类型补全HTML示例查看](/api.1473.cn/example/Array.htm)



