### 2.1.1 点对点获取同步的消息

由接入服务器请求存储服务器

返回的消息

```go
type HistoryMessage struct {
    MsgID    int64
    DeviceID int64 //消息发送者所在的设备ID
    Cmd      int32
    Raw      []byte
}

type PeerHistoryMessage struct {
    Messages  []*HistoryMessage
    LastMsgID int64
}
```



