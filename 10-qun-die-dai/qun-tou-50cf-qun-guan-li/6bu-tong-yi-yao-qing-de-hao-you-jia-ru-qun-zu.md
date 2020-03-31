### 2.不同意邀请的好友加入群组

所属服务：qim

提供对象：钱包app

开发者：cary

报错频率：

URL

```
/nacaiim/notAllowedJoinGroup
```

请求参数

    type NotAllowedJoinGroupReq struct {
    	From string `json:"from"`
    	InviteUid int64 `json:"invite_uid"`
    }

返回值

    type NotAllowedJoinGroupRes struct {
    	From string `json:"from"`
    	InviteUid int64 `json:"invite_uid"`
    }



