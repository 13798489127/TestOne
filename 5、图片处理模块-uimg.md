# 图片处理模块

---

* ## U.Img.Create

```
使用方法：U.Img.Create(UDE, UI, UME, UCB)

功能：创建图片浏览器功能区域

参数一：UDE {array}图片集合

参数二：UI {number}访问第几张图

参数三：UME {object}属性设置

参数四：UCB {function}设置回调函数
```

* ## 方法解释

#### 1、U.Img.Create.init

```
使用方法：U.Img.Create.init(UDE, UI, UME, UCB)

功能：创建图片浏览器功能区域

参数一：UDE {array} 图片集合

参数二：UI {number} 访问第几张图

参数三：UME {object} 属性设置

参数四：UCB {function} 设置回调函数
```

#### 2、U.Img.Create.init.prototype.ImgT\(\)

```
U.Img.Create.init.prototype.ImgT(UDE,UDID)

功能：创建图片

参数一：UDE {array}图片合集

参数二：UDID {number}访问第几张图
```

#### 3、U.Img.Create.init.prototype.Create\(\)

```
U.Img.Create.init.prototype.Create()

功能：创建图片浏览器
```

#### 4、U.Img.Create.init.prototype.XSI\(\)

```
U.Img.Create.init.prototype.XSI(UIOD,UT,UTF)

功能：删除图片窗体

参数一：UIOD {element}图片浏览器窗体

参数二：UT {number}图片浏览器对象

参数三：UTF {string}回调参数
```

#### 5、U.Img.Create.init.prototype.Wheel\(\)

```
U.Img.Create.init.prototype.Wheel(UT,UE)

功能：滚动放大缩小处理

参数一：UT {object}图片浏览器对象

参数二：UE {event}回调参数
```

#### 6、U.Img.Create.init.prototype.Change\(\)

```
U.Img.Create.init.prototype.Change(UTF,UT,UCB)

功能：切换图片的上一张或下一张
参数一：UTF {number}上/下一张的区分

参数二：UT {object}图片浏览器对象

参数三：UCB {function}回调参数
```

#### 7、U.Img.Create.init.prototype.Zoom\(\)

```
U.Img.Create.init.prototype.Zoom(US,UIOD,UT)

功能：放大缩小

参数一：US {string}上传成功回调函数

参数二：UIOD {number}上传成功回调函数

参数三：UT {function}回调函数
```

#### 8、U.Img.Create.init.prototype.PJ\(\)

```
U.Img.Create.init.prototype.PJ(UW,UH,UIOD,UIID)

功能：图片定位调整

参数一：UW {number}图片浏览器长度

参数二：UH {number}图片浏览器宽度

参数三：UIOD {element}图片浏览器

参数四：UIID {element}图片
```

#### 9、U.Img.Create.init.prototype.Rotate\(\)

```
U.Img.Create.init.prototype.Rotate(UV, UIOD, UT)

功能：图片角度设置

参数一：UV {string}上传成功回调函数

参数二：UIOD {number}上传成功回调函数

参数三：UT {function}回调参数
```

#### 10、U.Img.Create.init.prototype.MoveScroll\(\)

```
U.Img.Create.init.prototype.MoveScroll(UDOD, UT)

功能：浏览点移动

参数一：UDOD {element}图片窗体

参数二：UT {object}图片浏览器
```

#### 11、U.Img.Create.init.prototype.Move

```
U.Img.Create.init.prototype.Move(UDOD, UX, UY, UTL, UT)

功能：移动浏览

参数一：UDOD {element}图片窗体

参数二：UX {number}窗体left值

参数三：UY {number}窗体top值

参数四：UTL {array}所在区域滚动条

参数五：UL {object}图片浏览器
```

#### 12、U.Img.Create.init.prototype.Up

```
U.Img.Create.init.prototype.Up(UDOD)

功能：取消滚动

参数一：UDOD {string}上传成功回调函数
```

#### 13、U.Img.Create.init.prototype.Close

```
U.Img.Create.init.prototype.Close(UIOD, UT, UTF)

功能：移除窗口或者隐藏窗口

参数一：UIOD {element}窗体对象

参数二：UT {object}图片浏览器对象

参数三：UTF {boolean}是否移除还是隐藏
```

#### 14、U.Img.Create.init.prototype.Ready

```
U.Img.Create.init.prototype.Ready(UIOD, UIID, T, UDE)

功能：图片获取具体尺寸

参数一：UIOD {string}图片窗体

参数二：UIID {number}图片区域

参数三：T {function}图片浏览器对象

参数四：UDE {object}图片对象
```

#### 15、U.Img.Create.init.prototype.Load

```
U.Img.Create.init.prototype.Load(UIOD, UIID, T, UDE)

功能：图片缓冲

参数一：UIOD {element}图片浏览器窗体

参数二：UIID {element}图片元素

参数三：T {object}回调参数
参数四：UDE {function}回调参数
```

#### 16、U.Img.Create.init.prototype.Error

```
U.Img.Create.init.prototype.Error(URL, ITF)

功能：图片加载失败

参数一：URL {string}上传成功回调函数

参数二：ITF {number}上传成功回调参数
```



