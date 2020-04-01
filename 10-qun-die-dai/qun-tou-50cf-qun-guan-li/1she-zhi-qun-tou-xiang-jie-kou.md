### 设置群头像和群名称

所属服务：qim

提供对象：钱包app

开发者：cary

报错频率：

URL

```
/nacaiim/setGroupName
```

请求参数

    type SetGroupNameReq struct {
        From    string `json:"from"` //区块链账号
        Uid     int64  `json:"uid"`  //自己的imuid
        Groupid int64  `json:"groupid"` //群组的id
        Name    string `json:"name"`    //群名称
        Head    string `json:"head"`    //头像路径
    }

返回值

    type SetGroupNameRes struct {
        Groupid int64  `json:"groupid"`
        Name    string `json:"name"`
        Head    string `json:"head"`
    }



