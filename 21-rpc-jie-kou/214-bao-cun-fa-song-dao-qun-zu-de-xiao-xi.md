### 2.1.4  保存发送到群组的消息

当用户发送消息到群组时，需要调用这个接口

之前的接口返回参数

```go
func SaveGroupMessage(addr string, m *common.GroupMessage) (int64, error) {
}
```

需要增加返回个Offset的参数。在成功保存消息后，需要将Offset返回给RPC 的调用方。

```go
func SaveGroupMessage(addr string, m *common.GroupMessage) (int64,int64, error) {
}
```

调用方

```go
    msgid,offset, premsgID,err := SaveGroupMessage(p.appid, msg.ToGroupid, p.device_ID, m)
```



