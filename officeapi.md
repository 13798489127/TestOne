# Office-Api说明

---

## 1、U.D.E.GetSelectionRange

### a\)描述

生成光标处理函数，此处为云端编辑器光标处理的主要接口，调用该接口时建议用一个变量保存改光标值，以备下次使用的时候继续使用，例如U.D.Range = U.D.E.GetSelectionRange\(window , Element, object\);

### b\)参数列表

```
参数一：UDW（window）

     当前所在的window层

参数二：UDOD（element）

     需要光标控制的元素

参数三：UDE（object）

     需要传参的对象，形式为{CB:光标和键盘控制的回调函数, TF:该光标的唯一识别码}
```

### c\)返回参数\(U.D.E.SelectionRange\)

返回光标使用的对象（U.D.E.SelectionRange对象）



## 2、U.D.Range.Parent

### a\)描述

获取编辑光标所在的元素区域。

### b\)参数列表

```

参数一：UDR（光标对象U.D.Range）

       需要操作的光标对象，默认不传，默认为初始化对象。

参数二：UTF（Boolean）

       判断是否不获取#text对象直接获取文字所在的元素。
       
```

### c\)返回参数\(null\)

无



## 3、U.D.Range.Replace

### a\)描述

替换当前选中的文字，重新用新的文本或者是元素替换。

### b\)参数列表

```

参数一：UTS（需要替换的文本String）

       需要给选取替换的文字。
       
参数二：UDR（光标对象U.D.E.SelectionRange）

       判断是否不获取#text对象直接获取文字所在的元素。

参数三：UTF（是否聚焦到最后Boolean）

       是否保持原有的选择状态，还是聚焦到文字后面。
       
```

### c\)返回参数\(U.D.E.SelectionRange\)

返回光标使用的对象（U.D.E.SelectionRange对象）



## 4、U.D.Range.QX

### a\)描述

设置元素选取，给选取文字标蓝。

### b\)参数列表

```

参数一：US（选中文字开始的位置Number）

       选区开始的位置。
       
参数二：UE（选中文字结束的位置Number）

       选区结束的位置。
       
参数三：UDOD（选中的文字Element）

       选择的元素。
       
```

### c\)返回参数\(U.D.E.SelectionRange\)

光标选取对象（U.D.E.SelectionRange）



## 5、U.D.Range.SL

### a\)描述

直接选择指定的元素，设置该元素选区。

### b\)参数列表

```

参数一：UDOD（选择的元素Element）

       需要选择的元素。

参数二：UDR（光标编辑对象U.D.E.SelectionRange）

       选区结束的位置。
       
```

### c\)返回参数

光标选取对象（Range对象）



## 6、U.D.Range.GetSelectedHtml

### a\)描述

获取元素选取的html值，如果没有指定的html值就获取选取文本。

### b\)参数列表

```

参数一：UDR（光标编辑对象U.D.E.SelectionRange）

       光标对象处理，默认是不需要传参。
       
```

### c\)返回参数\(String\)

返回光标选中的元素文本值

# 7、U.D.Range.GetSelectedText

## a\)描述

获取元素选取的text值，只获取纯文本值，不包含元素值。

## b\)参数列表

### 参数一：UDR（光标编辑对象U.D.E.SelectionRange）

光标对象处理，默认是不需要传参。

## c\)返回参数\(String\)

返回光标选中的元素文本值



# 8、U.D.Range.SetStyle

## a\)描述

配置传入的文字样式

## b\)参数列表

### 参数一：UDR（光标编辑对象U.D.E.SelectionRange）

光标对象处理，默认是不需要传参。

## c\)返回参数\(String\)

返回光标选中的元素文本值



# 9、U.D.Range.writeStyle

## a\)描述

把传入的元素和样式值结合设置样式

## b\)参数列表

### 参数一：UDR（光标编辑对象U.D.E.SelectionRange）

光标对象处理，默认是不需要传参。

## c\)返回参数\(null\)

无



# 10、U.D.Range.Copy

## a\)描述

把文本位置复制到剪切板里

## b\)参数列表

### 参数一：UTH（需要复制的文本String）

光标对象处理，默认是不需要传参。

## c\)返回参数\(null\)

无



# 11、U.D.Range.Paste

## a\)描述

把文本粘贴到剪切板里

## b\)参数列表

### 参数一：UDOD（剪切到的元素Element）

需要剪切到的元素。

## c\)返回参数\(null\)

无



# 12、U.D.Range.GetGBWZ

## a\)描述

获取当前光标到指定元素选中的文字和图片的数量

## b\)参数列表

### 参数一：UDOD（剪切到的元素Element）

需要从当前光标到指定位置的元素

### 参数二：UTF（到指定元素判断Boolean）

判断是到指定元素的开头还是结尾。



## c\)返回参数\(Number\)

返回光标到指定元素的位置的长度。图片算1



# 13、U.D.Range.IsP

## a\)描述

判断传入的光标和当前光标是否在统一范围内

## b\)参数列表

### 参数一：UDR（光标元素Range）

需要判断的光标元素



## c\)返回参数\(Boolean\)

是否在指定的区域里



# 14、U.D.Range.IsE

## d\)描述

判断元素是否在指定的光标区域里

## e\)参数列表

### 参数二：UDOD（元素Element）

需要判断的元素，判断该元素是否在指定的区域里。



## f\)返回参数\(Boolean\)

是否在指定的区域里



