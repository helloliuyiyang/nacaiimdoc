### **2.群单聊开关设置**

所属服务：qim

提供对象：钱包app

开发者：devil

报错频率：

URL

```
/nacaiim/setGroupLimitFriend
```

请求参数

    type SetGroupLimitFriendReq struct {
        //From        string `json:"from"`
        Uid         int64  `json:"uid"`
        Groupid     int64  `json:"groupid"`
        LimitFriend int32  `json:"limit_friend"` //0:不限制 1：限制 （单聊加好友）
    }

返回值

    type SetGroupLimitFriendRes struct {
        Groupid     int64 `json:"groupid"`
        LimitFriend int32 `json:"limit_friend"` //0:不限制 1：限制 （单聊加好友）
    }



