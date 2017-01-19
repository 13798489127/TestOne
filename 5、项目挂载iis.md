# 项目挂载iis {#项目挂载iis}

---

### 1、点击windows--&gt;在计算机上右键–&gt;点击管理 {#1、点击windows--在计算机上右键–点击管理}

![](https://13798489127.gitbooks.io/uform/content/assets/image054.png)

### 2、在服务和应用程序中找到Internet信息服务（IIS）管理器 {#2、在服务和应用程序中找到internet信息服务（iis）管理器}

![](/Image/image055.png)

### 3、以下三个参数填写好点击确认 {#3、以下三个参数填写好点击确认}

![](/Image/image056.png)

> www.1473.cn示例

![](https://13798489127.gitbooks.io/uform/content/assets/image057.png)

> main.1473.cn示例

![](/Image/image059.png)

物理路径：

![](/Image/image058.png)

### 4、Main项目设置 {#4、main项目设置}

> 需要设置启动项目（UseStudio.Main）和起始文件（Crossdomain.htm）

![](/Image/image060.png)

### ![](https://13798489127.gitbooks.io/uform/content/assets/image061.png)

### 5、配置hosts文件 {#5、配置hosts文件}

> 打开hosts文件编辑在一下目录C:\Windows\System32\drivers\etc双击打开hosts

![](/Image/image062.png)

> 编辑hosts文件

![](https://13798489127.gitbooks.io/uform/content/assets/image063.png)

### 6、Manage项目直接在浏览器访问你设置好的iis网站域名 {#6、manage项目直接在浏览器访问你设置好的iis网站域名}

![](/Image/image064.png)

### 7、启动Main项目在浏览器中范围为空白页面且无报错即为挂载成功 {#7、启动main项目在浏览器中范围为空白页面且无报错即为挂载成功}

![](/Image/image065.png)

### 8、Main在VS中Mian.ashx\(.cs\)文件中设置断点 {#8、main在vs中mianashxcs文件中设置断点}

> 按F5进入调试模式可以调试即可查看项目运行

![](/Image/image066.png)

### 9、相关报错添加电脑用户 {#9、相关报错添加电脑用户}

![](https://13798489127.gitbooks.io/uform/content/assets/image067.png)

打开源代码中的Web.config文件找到框中的一行![](/Image/image068.png)

##### 如果出现该错误，解决方法如下： 在计算机新建一个usestudio的用户密码为usestudio-1的账户 {#如果出现该错误，解决方法如下：--在计算机新建一个usestudio的用户密码为usestudio-1的账户}

> 打开控制面板，点击添加或删除用户账户

![](https://13798489127.gitbooks.io/uform/content/assets/image069.png)

> 选择创建一个新账户

![](/Image/image070.png)

> 账户名为usestudio权限为管理员账户

![](/Image/image071.png)

> 点开用户，选择添加密码，密码为usestudio-1

![](/Image/image072.png)

#### 至此Manage项目重新执行步骤6即可，Main项目执行步骤7，8即可 {#至此manage项目重新执行步骤6即可，main项目执行步骤7，8即可}



