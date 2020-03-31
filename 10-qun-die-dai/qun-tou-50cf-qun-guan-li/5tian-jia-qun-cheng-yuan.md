### 2.添加群成员

所属服务：qim

提供对象：钱包app

开发者：cary

报错频率：

URL

```
/nacaiim/addGroupMember
```

请求参数

    type AddGroupMemberReq struct {
        From         string  `json:"from"`
        Uid          int64   `json:"uid"`
        Groupid      int64   `json:"groupid"`
        UidArrays    []int64 `json:"uid_arrays"` //邀请成员的数组
        MsgType      string  `json:"msg_type"`//忽略
        OldUidArrays []int64 `json:"old_uid_arrays"`//忽略
        //群主uid
        OwnerUid int64 `json:"owner_uid"` //群主的imuid
        //group_name
        GroupName string `json:"group_name"`
    }

返回值

    type AddGroupMemberRes struct {
        Groupid  int64 `json:"groupid"`
        Imuserid int64 `json:"im_userid"`
    }



