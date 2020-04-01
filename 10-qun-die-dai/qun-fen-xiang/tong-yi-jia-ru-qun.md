### 群主确认加入

所属服务：qim

提供对象：钱包app

开发者：tom

报错频率：

URL

```
/nacaiim/joinGroupConfirm
```

请求参数

    type JoinGroupConfirmReq struct {
    	//群ID
    	GroupId int64 `json:"group_id"`
    	//申请ID
    	JoinId []int64 `json:"join_id"`
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



