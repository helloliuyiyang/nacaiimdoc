### **3.查询群单聊和禁言状态**

所属服务：qim

提供对象：钱包app

开发者：devil

报错频率：

URL

```
/nacaiim/getGroupSetup
```

请求参数

    type GetGroupSetupReq struct {
        Groupid   int64  `json:"groupid"`
    }

返回值

    type GetGroupSetupRes struct {
        Groupid   int64 `json:"groupid"`
        LimitChat int32 `json:"limit_chat"` //禁言
        LimitFriend int32 `json:"limit_friend"` //单聊&不可加好友
        InviteSwitch int64 `json:"invite_switch"` //群邀请开关
    }



