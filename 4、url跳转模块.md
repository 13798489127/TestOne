# url跳转模块

---

1、U.M.QueryString\(UK,\)

```
功能：获取URL参数

参数一:string QuerySting key  键值

返回值:string 获取key对应的值

示例：

当前url : http://www.1473.cn/userpages/U_OF.aspx?FildID=f50f6551-d486-48a0-8ec8-f628f3718455

执行此函数获得url里面的参数：U.M.QueryString("FildID")
```

2、U.M.GetUF\(\)

```
功能：获取用户获取的地址

示例：

    当前Url: http://www.1473.cn/#!/disk/13798489127/f6d7a4b6-e34c-4964-beed-24187b2cb1ba

    执行此函数获取用户获取的地址: U.M.GetUF()

    返回值：["#!", "disk", "13798489127", "f6d7a4b6-e34c-4964-beed-24187b2cb1ba"]
```



