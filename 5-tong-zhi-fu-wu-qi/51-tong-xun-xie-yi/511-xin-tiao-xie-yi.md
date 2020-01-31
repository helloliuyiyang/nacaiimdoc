## 5.1.1  心跳协议

客户端和通知服务器的心跳协议，是携带了数据的，和我们通用定义的心跳不一样。这个心跳是携带了数据，在客户端和服务端直接不断的交互互相的同步数据的偏移。客户端带上本地的数据的同步偏移，服务端在心跳回应中发送这个用户的同步偏移。这个同步偏移的数据是指点对点的同步。

![](/assets/syncNotifyProtocol.png) 心跳PING的PB

```
// 消息结构.
message UserMsgSyncInfo {
    int64 GroupId = 1;
    int64 SyncKey = 2;
    int64 OffSet = 3;
}
```

回应PONG的PB

```
// 消息结构.
message UserMsgSyncInfo {
    int64 GroupId = 1;
    int64 SyncKey = 2;
    int64 OffSet = 3;
}
```



