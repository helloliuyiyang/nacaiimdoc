### 获取群分享连接

所属服务：qim

提供对象：钱包app

开发者：tom

报错频率：

URL

```
/nacaiim/createGroupShare
```

请求参数

    type GroupShareReq struct {
        //连接申请人ID
        Uid         int64  `json:"uid"`
        //组id
        Groupid      int64   `json:"group_id"`
    }

返回值

```
//允许继续浏览查看
{
    "code": 200,
    "message": "OK",
    //用于加入群的参数    
    "data": "对象信息加密后再做base64"
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



