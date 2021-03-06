## 5.1.3 点对点的同步通知带数据

当用户A 发送一条消息给B，发到接入服务器时，接入服务器或者路由服务，将给B 发送一条通知，通知这个用户有条新的消息。

这个和5.1.2 的区别是,这个同步通知就直接带了点对点的下发消息。由服务端直接进行了PUSH。这个PUSH 到客户端失败也没关系。

客户端还会对本地的数据进行检查是否连续，不连续，客户端会进行次拉取。在大多数情况下，这个消息就直接PUSH 到客户端就能确保客户端的本地消息是连续的了。不再需要客户端进行次主动同步拉取。

![](/assets/peerSyncNotifySeq.png)

3:通知服务器发送给客户端的事件为\(IM\_CMD\_NOTIFY\_SYNC\_HAS\_CHATDATA=337\)

这个消息带的PB 为 ImClientSendMsg

```go
message ImSyncNotifyWithData {
int64 offset=1;
int64 nextSynckey=2;
int64 fromUID=3;
int64 toUID=4;
int32 timestamp=5;
int32 synckey=6;
int32 len=7;
int32 msgType=8;
int32 msgFlag=9;
int64 preSynckey=10;
bytes content=11;
}
```

 协议文件路径为

gopath/src/nacaiim/protoc/msg.proto

| 字段 | 备注 |
| :--- | :--- |
| offset | 用户的消息偏移 |
| nextSynckey | 下一个同步的偏移 |
| fromUID | 发送消息的用户ID |
| toUID | 接收消息的用户ID |
| timestamp | 发送消息的时间戳 |
| synckey | 这个消息的同步的key |
| len | 这个消息的内容长度 |
| msgType | 这个消息的类型msg |
| msgFlag | 消息的标记 |
| preSyncKey | 前一个同步KEY |
| content | 消息的内容 |



