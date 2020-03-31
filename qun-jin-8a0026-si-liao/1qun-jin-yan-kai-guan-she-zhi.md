### **1.群禁言开关设置**

所属服务：qim

提供对象：钱包app

开发者：devil

报错频率：

URL

```
/nacaiim/setGroupLimitChat
```

请求参数

    type SetGroupLimitChatReq struct {
        //From      string `json:"from"`
        Uid       int64  `json:"uid"`
        Groupid   int64  `json:"groupid"`
        Limitchat int32  `json:"limitchat"`
    }

返回值

    type SetGroupLimitChatRes struct {
        Groupid   int64 `json:"groupid"`
        Limitchat int32 `json:"limitchat"`
    }



