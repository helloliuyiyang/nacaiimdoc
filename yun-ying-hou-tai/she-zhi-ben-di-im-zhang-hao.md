### **设置本地IM账号**

json结构：

```
{
    "api_name":"set_im_user_no,
    "no":1,
    "passwd":"string",
    "imuid":1
}
```

信息字段含义：

| 字段 | 含义 |
| :--- | :--- |
| api\_name | 调用API名称 |
| no | 账号 |
| passwd | 密码 |
| imuid | 用户ID |

回应消息

```
{
    "api_name":"set_im_user_no,
    "code":200,
    "desp":"OK",

}
```

回应消息api\_name 代表当前调用的那个函数。

code代表这个消息的调用结果。200 为成功

desp为调用失败，就是code 为非200 的描述信息。

