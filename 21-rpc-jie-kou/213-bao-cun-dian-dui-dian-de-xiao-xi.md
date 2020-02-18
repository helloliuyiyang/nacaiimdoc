### 2.1.3 保存点对点的消息

当用户进行点对点的消息发送时，需要调用这个SaveMessage的接口保存消息

之前的接口返回参数

```go
func SavePeerMessage(addr string, m *common.PeerMessage) (int64, error) {
}
```

需要增加返回个Offset,上一个偏移，的参数。在成功保存消息后，需要将Offset返回给RPC 的调用方。

```go
func SavePeerMessage(addr string, m *common.PeerMessage) (int64, int64,error) {
}
```

调用方

```go
    msgid,offset, premsgID,err := SaveMessage(client.appid, msg.sender, client.device_ID, m)
```

msgid,是这个消息在磁盘上存储的位置\(synckey\)

premsgID,是这个消息在磁盘上存储的上一调消息的位置\(synckey\)

offset,是这个消息在磁盘上存储的这个用户，连续按顺序递增，1，2，3，4 这样的一个序列号。





