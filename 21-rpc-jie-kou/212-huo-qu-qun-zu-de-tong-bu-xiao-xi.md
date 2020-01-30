### 2.1.2 获取群组的同步消息

由接入服务器请求存储服务器，获取群组的消息

返回的消息

```go
type PeerHistoryMessage struct {
	Messages  []*HistoryMessage
	LastMsgID int64
}

type GroupHistoryMessage PeerHistoryMessage
```



