# 概括\(讲课人：林志雄，Time：5/19\)

```
在我们做网页的时候，一个不规范的布局，放在不同浏览器浏览效果会有差异性
和兼容性。
通常在我们做网页布局的时候，一个好的布局很帮助我们解决很多兼容性的问题！
```

# 怎么布局?

```
//首先看一个图，跟着这句布局图来布局
```

## HTML + CSS 练习（讲课人：徐杰锋 Time：6/2）

## CSS（讲课人：陈坤彬 Time：6/1）

```
<style type="text/css">
    * { padding: 0; margin: 0; }
    .BG { background-color: #383838; width: 1100px; height: 760px; margin: 0 auto; }
    .div1 { width: 800px; height: 50px; float: left; margin-left: 150px; margin-top: 40px; 
    float: left; }
    .logo { border-radius: 100px; background-color: #fff; width: 28px; height: 28px;
     margin-top: 5px; float: left; }
    .text1 { font-size: 30px; color: #fff; font-weight: bold; float: left; margin-left: 20px; }
    .text2 { font-size: 15px; color: #fff; float: right; line-height: 50px; margin-right: 30px; }
    .right { border-radius: 50px; border: 1px solid #fff; width: 110px; height: 40px; 
    float: right; margin-top: 3px; }
    .text3 { font-size: 18px; color: #fff; margin-left: 22px; margin-top: 10px; }
    .div2 { width: 650px; height: 220px; float: left; margin-left: 225px; margin-top: 140px; }
    .text4 { font-size: 48px; color: #fff; font-weight: bold; text-align: center; }
    .g { border-radius: 50px; background-color: #74c602; width: 158px; height: 55px; 
    margin-left: 246px; margin-top: 50px; }
    .text5 { font-size: 22px; color: #fff; line-height: 55px; margin-left: 53px; }
    .div3 { border-radius: 5px; background-color: #383838; border: 1px solid #919191;
     width: 800px; height: 250px; float: left; margin-left: 150px; margin-top: 58px; }
    .div4 { border-radius: 5px 5px 0 0; background-color: #434343; width: 800px; 
    height: 50px; float: left; }
    .yuan_div { width: 50px; height: 20px; margin-left: 20px; margin-top: 15px; }
    .yuan1 { border-radius: 100px; background-color: red; width: 8px; height: 8px; 
    margin-top: 5px; float: left; }
    .yuan2 { border-radius: 100px; background-color: orange; width: 8px; height: 8px; 
    margin-top: 5px; float: left; margin-left: 9px; }
    .yuan3 { border-radius: 100px; background-color: #74C502; width: 8px; height: 8px;
     margin-top: 5px; float: left; margin-left: 9px; }
    .div5 { width: 700px; height: 110px; margin-left: 50px; margin-top: 45px; float:
     left; }
    .dy1 { background-color: #fff; width: 90px; height: 90px; border-radius: 100px; 
    float: left; }
    .xy_div { width: 90px; height: 90px; margin-left: 25px; float: left; margin-top: 10px; }
    .xy1 { background-color: #fff; width: 55px; height: 55px; border-radius: 100px;
     margin: 0 auto; }
    .xy_text { font-size: 13px; color: #EF4627; text-align: center; font-weight: 
    bold; margin-top: 5px; }
    .xy2 { background-color: #fff; width: 55px; height: 55px; border-radius: 100px;
     margin: 0 auto; }
    .dy2 { background-color: #fff; width: 90px; height: 90px; border-radius: 100px;
     float: left; margin-left: 20px; }
    .dy3 { background-color: #fff; width: 90px; height: 90px; border-radius: 100px;
     float: left; margin-left: 40px; }

</style>
```

## HTML布局\(3\)

```
<body>
    <div class="BG">
        <div class="div1">
            <div class="logo">
            </div>
            <div class="text1">
                heyfitty
            </div>
            <div class="right">
                <div class="text3">
                    Sign in
                </div>
             </div>
             <div class="text2">
                 Already a member?
             </div>
        </div>
    <div class="div2">
        <div class="text4">
            <p>Cheeky Kiss the Hottest,</p>
            Hangout with the Coolest!
        </div>
        <div class="g">
            <div class="text5">
                Join
            </div>
        </div>
    </div>
    <div class="div3">
        <div class="div4">
            <div class="yuan_div">
                <div class="yuan1">
                </div>
                <div class="yuan2">
                </div>
                <div class="yuan3">
                </div>
            </div>
        </div>
            <div class="div5">
                <div class="dy1">
                </div>
                <div class="xy_div">
                    <div class="xy1">
                    </div>
                    <div class="xy_text">
                         Cheeky Kissed
                    </div>
                </div>
                <div class="dy2">
                </div>
                <div class="dy3">
                </div>
                <div class="xy_div">
                    <div class="xy1">
                    </div>
                    <div class="xy_text">
                         Hung out with
                    </div>
                </div>
                <div class="dy3">
                </div>
            </div>
        </div>
    </div>
</body>
```

## CSS

```
<
style type="text/css"
>

    * { margin: 0px; padding: 0px; }
    .main { margin: 0 auto; width: 100%; background: #eeeeee; height: 100%; }
    .header { background: #e7613f; height: 110px; color: White; padding-left: 50px; }
    .h_title { font-size: 25px; font-family: 微软雅黑; font-weight: bold; padding-top: 20px; }
    .h_text { padding-top: 10px; font-size: 14px; color: #eeeeee !important; }
    .mainContent { padding-top: 20px; }
    .Content-left { margin-right: 300px; margin-left: 50px; }
    .Content-left div { float: left; }
    .Content-right { width: 300px; float: right; margin-right: 50px; color: #404040; }
    .box { width: 200px; height: 200px; border: 2px solid #e5e5e5; background: white; 
    margin: 0 25px 25px 0; text-align: center; position: relative; }

<
/style
>
```

## HTML布局（2）

```
<body>
    <div class="main">
        <div class="header">
            <div class="h_title">
                CSS Explain
            </div>
            <div class="h_text">
                15 simple CSS Explain and throbbers CSS and minimal HTML
            </div>
        </div>
        <div class="mainContent">
            <div class="Content-right">
                If someone loves a flower, of which just one single blossom grows in all the millions and 
                <span style="color: blue;">millions of stars,</span>it is enough to make him
                happy just to look at the stars. He can say to himself, "Somewhere, my flower is
                there…" But if the sheep eats the flower, in one moment all his stars will be 
                <span style="color: blue;">darkened...</span>And you think that is not important!
            </div>
            <div class="Content-left">
                <div class="box">
                    <img src="../img/1.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; 
                    margin-bottom: 15px; ">
                        I am firm
                    </div>
                </div>
                <div class="box">
                    <img src="../img/2.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; 
                    margin-bottom: 15px;">
                        I am music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/3.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; 
                    margin-bottom: 15px;">
                        I am music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/4.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center;
                     margin-bottom: 15px;">
                        I m music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/5.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; margin-bottom: 15px;">
                        I am music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/6.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; margin-bottom: 15px;">
                        I am music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/7.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; margin-bottom: 15px;">
                        I am music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/8.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; margin-bottom: 15px;">
                        I am music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/9.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; margin-bottom: 15px;">
                        I am music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/10.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; margin-bottom: 15px;">
                        I am music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/11.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; margin-bottom: 15px;">
                         I am music
                    </div>
                </div>
                <div class="box">
                    <img src="../img/12.png" style="width: 50px; height: 50px; padding-top: 50px;">
                    <div style="position: absolute; bottom: 0px; width: 200px; text-align: center; margin-bottom: 15px;">
                         I am music
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
```

## CSS样式

```
<style type="text/css">

    /*里面内容为注释*/
    /*每个div自己为一行（在没有float属性之前）*/
    .div1{width:500px;height:100px;}
    /*div2 宽度为500px，高度为200px，背景颜色为绿色，浮动，左外边距为50px*/
    .div2{width:700px;height:100px;margin-top:10px;}
    /*div2里面创建了div21和div22让他们具有浮动效果(float:left),div2和div21、div22具有包含关系*/
    .div21{width:225px;height:225px;background-color:green;float:left;}
    .div22{width:225px;height:225px;background-color:green;float:left;margin-left:20px;}
    .div11{width:100px;height:100px;background-color:blue;float:left;margin-left:30px;}
    .div3{margin-top:10px;}


    /*常规页面的基本构造*/
    .header{width:800px;height:200px;background-color:green;}
    .bodya{width:800px;height:400px;margin-top:10px;}
    .footer{width:800px;height:100px;background-color:pink;margin-top:10px;}
    .b1{width:350px;height:400px;background-color:blue;float:left;}
    .b2{width:350px;height:400px;background-color:blue;float:left;margin-left:100px;}
    .tiao{width:300px;height:100px;margin-left:25px;margin-top:30px;background-color:gray;}

</style>
```

## HTML布局

```
<body>
    <div class="header">
    </div>
    <div class="bodya">
        <div class="b1">
            <div class="tiao">
            </div>
            <div class="tiao">
            </div>
            <div class="tiao">
            </div>
        </div>
        <div class="b2">
            <div class="tiao">
            </div>
            <div class="tiao">
            </div>
            <div class="tiao">
            </div>
        </div>
    </div>
    <div class="footer">
    </div>
</body>
```



