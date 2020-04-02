### 申请加入群

所属服务：qim

提供对象：钱包app

开发者：tom

报错频率：

URL

```
/nacaiim/joinGroupShare
```

请求参数

    type JoinGroupShareReq struct {
        //进群人ID
        Uid         int64  `json:"uid"`
        //之前分享的连接加密字符串
        Url      string   `json:"url"`
        //进群渠道
        MsgType      string   `json:"msg_type"`

    }

返回值

```
//允许继续浏览查看
{
    "code": 200,
    "message": "OK",

    "data": ""
}
//异常情况1
{
    "code": 403,
    "message": "该功能未开发,请联系开发者",    
    "data": ""
}
//异常情况2
{
    "code": 403,
    "message": "无权限使用,请联系开发者",    
    "data": ""
}
```



