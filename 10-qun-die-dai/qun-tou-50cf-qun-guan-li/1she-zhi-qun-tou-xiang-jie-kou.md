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
        From    string `json:"from"`
        Uid     int64  `json:"uid"`
        Groupid int64  `json:"groupid"`
        Name    string `json:"name"`
        Head    string `json:"head"`
    }

返回值

    type SetGroupNameRes struct {
        Groupid int64  `json:"groupid"`
        Name    string `json:"name"`
        Head    string `json:"head"`
    }



