### 5.1.4  群组同步通知

用户A 向群组发送消息,access\_server 收到消息，保存后，给群组里的每个用户发个更新通知。

同5.1.2和5.1.3的流程一样。

![](/assets/groupSyncNotify.png)

3:通知服务器给客户端的群组同步通知\(IM\_CMD\_GROUP\_NOTIFY\_SYNC=336\)

这个消息带的包体为

```go
// 消息结构.
message UserMsgSyncInfo {
    int64 GroupId = 1;
    int64 SyncKey = 2;
    int64 OffSet = 3;
}
```

 

