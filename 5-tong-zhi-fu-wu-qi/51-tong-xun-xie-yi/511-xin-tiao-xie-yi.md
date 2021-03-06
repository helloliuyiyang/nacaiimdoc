## 5.1.1  心跳协议

客户端和通知服务器的心跳协议，是携带了数据的，和我们通用定义的心跳不一样。这个心跳是携带了数据，在客户端和服务端直接不断的交换互相的同步数据的偏移。客户端带上本地的数据的同步偏移，服务端在心跳回应中发送这个用户的同步偏移。这个同步偏移的数据是指点对点的同步。

![](/assets/syncNotifyProtocol.png) 1: 客户端发送心跳 PING\(IM\_CMD\_HEART\_PING=301\) 消息。

 心跳的PB如下

```
// 消息结构.
message UserMsgSyncInfo {
    int64 GroupId = 1;
    int64 SyncKey = 2;
    int64 OffSet = 3;
}
```

2:服务端回应PONG\(IM\_CMD\_HEART\_PONG = 302\)消息。

心跳回应的PB如下

```
// 消息结构.
message UserMsgSyncInfo {
    int64 GroupId = 1;
    int64 SyncKey = 2;
    int64 OffSet = 3;
}
```

| 字段 | 备注 |
| :--- | :--- |
| Groupid | 这里为0，代表是个人点对点，pb3.0对0值不会进行编码 |
| SyncKey | 这个用户的全局的消息同步key |
| Offset | 这个用户的个人的消息的偏移id,是连续的 |



