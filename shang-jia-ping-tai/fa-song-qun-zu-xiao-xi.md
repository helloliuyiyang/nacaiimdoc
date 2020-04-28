### 发送群组消息

json格式：

```
{
    "api_name":"im_send_group_msg",
    "appmsgID":1,
    "repair_bill":"string",
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
| repair\_bill | 工单号 |
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

上面的是对API 调用的回应。

