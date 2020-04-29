### 6.3.11 发送图片消息

json格式：

```
{
    "api_name":"im_send_picture",
    "host":"string",
    "name":"string",
    "md5":"string",
    "msg_id":1,
    "total_len:"string"，
    “data”:byte
}
```

信息字段含义：

| 字段 | 含义 |
| :--- | :--- |
| api\_name | 调用API名称 |
| host | 图片服务器地址 |
| name | 图片名称 |
| md5 | 图片MD5 |
| msg\_id | 消息id |
| total\_len | 发送的byte数组的长度 |
| data | 传送的byte数组 |

```
{
    "api_name":"im_send_picture",
    "code":200,
    "desp":"OK",

}
```

上面的是对API 调用的回应。

