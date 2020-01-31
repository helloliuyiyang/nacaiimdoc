### 5.1.5 群组同步通知带数据

用户A 向群组发送消息,access\_server 收到消息，保存后，给群组里的每个用户发个更新通知，同时带上这条数据。

![](/assets/groupSyncNotifyWithData.png)

3:通知服务器给客户端的群组同步通知带上聊天消息\(IM\_CMD\_GROUP\_NOTIFY\_SYNC\_HAS\_CHATDATA = 338\)

这个消息的PB包体为

```js
message ImGroupSyncNotifyWithData {
int64 offset=1;
int64 nextSynckey=2;
int64 fromUID=3;
int64 ToGroupid=4;
int32 timestamp=5;
int64 synckey=6;
int32 len=7;
int32 msgType=8;
int32 msgFlag=9;
int64 preSynckey=10;
bytes content=11;
}
```

协议文件路径为

gopath/src/nacaiim/protoc/sync.proto

