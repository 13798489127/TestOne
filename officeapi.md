# 1、U.D.E.GetSelectionRange

## a\)描述

生成光标处理函数，此处为云端编辑器光标处理的主要接口，调用该接口时建议用一个变量保存改光标值，以备下次使用的时候继续使用，例如U.D.Range = U.D.E.GetSelectionRange\(window , Element, object\);

## b\)参数列表

```
参数一：UDW（window）

     当前所在的window层
     
参数二：UDOD（element）

     需要光标控制的元素
     
参数三：UDE（object）

     需要传参的对象，形式为{CB:光标和键盘控制的回调函数, TF:该光标的唯一识别码}
     
```

## c\)返回参数\(U.D.E.SelectionRange\)

返回光标使用的对象（U.D.E.SelectionRange对象）

