### 6.3.4 发送群组消息

func IMSendGroupMsg\(msg string\)//发送群组消息

json格式：

```
{
    "api_name":"im_send_group_msg",
    "appmsgID":1,
    "groupid":1,
    "msgType":1,
    "msgLen":1,
    "data:"string"
}
```

信息字段含义：

| 字段 | 含义 |
| :--- | :--- |
| api\_name | 调用API名称 |
| appmsgID | 消息ID |
| groupid | 群组ID |
| msgType | 消息类型 |
| msgLen | 消息长度 |
| data | 发送的数据 |

```
{
    "api_name":"im_send_group_msg",
    "code":200,
    "desp":"OK",

}
```



