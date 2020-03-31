### 2.设置开启群邀请确认

所属服务：qim

提供对象：钱包app

开发者：cary

报错频率：

URL

```
/nacaiim/setInviteSwitch
```

请求参数

    type SetInviteSwitchReq struct {
    	From string `json:"from"`
    	GroupId int64 `json:"group_id"`
    	InviteSwitch int64 `json:"invite_switch"`//0:关闭 1:打开
    }

返回值

    type SetInviteSwitchRes struct {
    	GroupId int64 `json:"group_id"`
    	InviteSwitch int64 `json:"invite_switch"`//0:关闭 1:打开
    }



