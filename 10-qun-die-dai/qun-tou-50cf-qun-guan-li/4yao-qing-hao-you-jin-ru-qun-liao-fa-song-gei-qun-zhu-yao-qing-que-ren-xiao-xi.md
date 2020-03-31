### 2.邀请好友进入群聊发送给群主邀请确认消息

所属服务：qim

提供对象：钱包app

开发者：cary

报错频率：

URL

```
/nacaiim/sendInviteFriendsToOwnerMsg
```

请求参数

    type InviteFriendsToOwnerGroupReq struct {
    	From               string               `json:"from"`
    	Uid                int64                `json:"uid"`
    	GroupId            int64                `json:"group_id"`             //群组id
    	OwnerUid           int64                `json:"owner_uid"`            //群主的uid
    	InviteReason       string               `json:"invite_reason"`        //邀请理由
    	InviteGroupFriends []InviteGroupFriends `json:"invite_group_friends"` //朋友的uid
    }

    type InviteGroupFriends struct {
    	FriendUid int64 `json:"friend_uid"`
    }

返回值

    type InviteFriendsToOwnerGroupRes struct {
    	Uid      int64 `json:"uid"`
    	GroupId  int64 `json:"group_id"`  //群组id
    	OwnerUid int64 `json:"owner_uid"` //群主的uid
    }



