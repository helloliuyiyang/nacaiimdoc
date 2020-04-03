### 2.查询群主是否开启邀请确认

所属服务：qim

提供对象：钱包app

开发者：cary

报错频率：

URL

```
/nacaiim/getInviteSwitch
```

请求参数

    type GetInviteSwitchReq struct {
        GroupId int64 `json:"groupid"`
    }

返回值

    type GetInviteSwitchRes struct {
        GroupId int64 `json:"groupid"`
        InviteSwitch int64 `json:"invite_switch"`
    }



