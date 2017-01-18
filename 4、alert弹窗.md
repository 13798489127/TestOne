# Alert弹窗

---

#### 方法一：无确认按钮—自动消失

函数：U.Alert\(c, t\);

参数一（c）：str弹窗内容

参数二（t）：int /ms毫秒alert的显示时间，默认显示1秒。

示例一（无确认按钮）：U.Alert\("www.1473.cn"\);

![](/Image/image097.png)

#### 方法二：有确认按钮，按确认消失

函数：U.Alert\(c, t, y\);

参数一（c）：str弹窗内容

参数二（t）：null保留

参数三（y）：Boolean是否有确认按钮默认false，为无确认按钮。

示例（有确认按钮）：U.Alert\("www.1473.cn", null, true\);

![](/Image/image098.png)

