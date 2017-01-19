# String数据类型补全 {#string数据类型补全}

---

#### 2.1.1、RFH（）该功能没有作用 {#211、rfh（）该功能没有作用}

```
功能:字符串输出
```

#### 2.1.2、Count\(\) {#212、count}

```
功能：返回字符串长度

参数：无参数

返回值：int

示例："123".Count()

结果: 返回3
```

#### 2.1.3、SubstrU（begin,end） {#213、substru（beginend）}

```
功能：截取字符串

参数：

    参数一: int：需要截取字符串的起点

    参数二: int：需要截取字符串的终点

返回值：String

示例："abcdf".substrU(1,3)

结果: "abc"
```

#### 2.1.4 、jsstring\(\) {#214-、jsstring}

```
功能：把所有的\r\n \n \”分别转换为\r\n\n\”（让换行符 双引号的转义符保留在原字符串）

参数：无参数

返回值：String

示例："12a\r\n\"aaa3".jsstring\(\)

结果："12a\r\n\"aaa3"
```

#### 2.1.5、SubstrN\(length\) {#215、substrnlength}

```
功能：判断字符串是否在指定长度内

参数：
      参数一: int：指定的长度

返回值：boolean

示例：  ”1234”.SubstrN\(3\)

      结果：  false

示例： ”1234”.SubstrN(4)

      结果： true
```

#### 2.1.6、StrIsNull\(\) {#216、strisnull}

```
功能：判断字符串是否为空

参数：无参数

返回值：boolean

示例：'    '.StrIsNull()

结果：true
```

#### 2.1.7 、SetNR\(\) {#217-、setnr}

```
功能:文本换行替换成页面换行

参数：无参数

返回值：string

示例："asd\r\nasd".SetNR()

结果："asd<br />asd"
```

#### 2.1.8 、SetBr\(\) {#218-、setbr}

```
功能：页面换行替换成文本换行

参数：无参数

返回值: string

示例："asd<br/>asd".SetBr()

结果："asd
asd"
```

#### 2.1.9 、SubN\(\) {#219-、subn}

```
//有错误 可能修改方案：.replace(/<(p)[^<>]*>/ig, "").replace(/<(\/p)[^<>]*>/ig, "")

功能:去除行 （去除字符串所有<p></p>标签）

参数：无参数

返回值:string

示例:"<p>123</p>".SubN()

结果:"123"
```

#### 2.1.10、SubBRNB\(\) {#2110、subbrnb}

```
功能:去除br和空格(br转换为 \r\n)

参数：无参数

返回值:string

示例:"<br/>123  &nbsp;".SubBRNB()

结果:"

123  "
```

#### 2.1.11、 IsGEdit\(\) {#2111、-isgedit}

```
功能:判断是否不为空

参数：无参数

返回值:boolean

示例:"<br/>\r\n".IsGEdit()

结果:false

示例：""<br/>ss\r\n"".IsGEdit()

结果：true
```

#### 2.1.12、 HTMLSign\(\) {#2112、-htmlsign}

```
功能:把文本的 &lt; &gt;转化成 <>

参数：无参数

返回值:string

示例:" &lt; &gt;".HTMLSign()

结果:" < >"
```

#### 2.1.13、 RemoveHTMLSign\(\) {#2113、-removehtmlsign}

```
功能:HTML字符转化为ASCLL码

参数：无参数

返回值:string

示例:"<div id='asd'>".RemoveHTMLSign()

结果:"&lt;div id=&#39;asd&#39;&gt;"
```

#### 2.1.14 、restore\(\) {#2114-、restore}

```
功能: 所有《》转换为<>

参数：无参数

返回值:string

示例:"《123》".restore();

结果:"<123>"
```

#### 2.1.15 、secure\(\) {#2115-、secure}

```
功能: 所有<>转换为《》

参数：无参数

返回值:string

示例:"<123>".secure()

结果:"《123》"
```

#### 2.1.16、encode\(\) {#2116、encode}

```
功能: 把字符串作为URI 组件进行编码

参数：无参数

返回值:string

示例:"阿萨德asd！！!!".encode()

结果:"%E9%98%BF%E8%90%A8%E5%BE%B7asd%EF%BC%81%EF%BC%81!!"
```

#### 2.1.17 、Trim\(\) {#2117-、trim}

```
功能:去除空白符号（空格、\t、\s、\r、\n）

参数：无参数

返回值:string

示例:"asd\r\n\t a".Trim()

结果:"asda"
```

#### 2.1.18、 Ltrim\(\) {#2118、-ltrim}

```
功能:去除左边空格

参数：无参数

返回值:string  

示例:"asd".Ltrim()

结果:"asd"
```

#### 2.1.19、 Rtrim\(\) {#2119、-rtrim}

```
功能:去除右边边空格

参数：无参数

返回值:string  

示例:"asd".Rtrim()

结果:"asd"
```

#### 2.1.20 、AddPreSpace\(n，str\) {#2120-、addprespacen，str}

```
功能:在后面加N个字符

参数：

     参数一: int：字符个数

     参数二: string：字符串

返回值:string 

示例:"abc".AddPreSpace(3,"d")

结果:"abcddd"
```

#### 2.1.21 、InsertStr\(str,index\) {#2121-、insertstrstrindex}

```
功能:指定位置插入字符串

参数：

     参数一:tring:插入的字符串

     参数二:插入的位置

返回值:string  

示例:"asd".InsertStr("890",1)

结果:"a890sd"
```

#### 2.1.22、AP\(index\) {#2122、apindex}

```
功能:指定位置插入省略号

参数：

     参数一:插入的位置

返回值: string  

示例:"abcdefg".AP(3)

结果:"abc..."
```

#### 2.1.23toInt\(\) {#2123toint}

```
功能:把字符串里的数字转化成int

参数：无参数

返回值: string  

示例:"1234".toInt()

结果:1234
```

#### 2.1.24、replaceAll\(s1,s2\) {#2124、replacealls1s2}

```
功能:把指定的字符串转换为指定字符串

参数：

    参数一：原字符串包含的字符串

    参数二：需要替换的字符串

返回值: string

示例:"12345".replaceAll("23","a")
```

结果:"1a45"

#### 2.1.25、parseJSON（） {#2125、parsejson（）}

```
功能：把json格式的字符串转换成json

参数：json格式的字符串

返回值:json

示例:"{a:123}".parseJSON();

结果:{a: 123}
```

#### 2.1.26capital（） {#2126capital（）}

```
功能:首字母大写

参数：无参数

返回值:string 

示例:”asd”.capital()

结果:”Asd”
```

#### 2.1.27、SplitRN（） {#2127、splitrn（）}

```
功能:根据换行分类

参数：无参数

返回值:Array  

示例:"asd\nqwe\r\nqweqwe".SplitRN()

结果:["asd", "qwe", "qweqwe"]
```

#### 2.1.28、SplitHTML\(\) {#2128、splithtml}

```
功能:根据标签分类 （标签指 =》 <>）

参数：无参数

返回值:Array

示例:"<p>asd</p>asd<br/>".SplitHTML()

结果:["<p>", "asd", "</p>", "asd", "<br/>"]
```

#### 2.1.29、ReplaceHTML（） {#2129、replacehtml（）}

```
功能:过滤标签留下纯文本

参数：无参数

返回值:string

示例:"<p>asd</p>asd<br/>".ReplaceHTML()

结果:"asdasd"
```

#### 2.1.30、 toTxt（） {#2130、-totxt（）}

```
功能:根据html内容转换成txt格式

参数：无参数

返回值:string

示例:"<p>asd</p>asd<br/>".toTxt()

结果:"asd

asd"
```

---

[String数据类型补全HTML示例查看](/api.1473.cn/example/String.htm)

### 



