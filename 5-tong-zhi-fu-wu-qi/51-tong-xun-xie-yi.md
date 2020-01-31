## 5.1 通讯协议

通知服务器和客户端的接口有多种有基于protobuf 的二进制流协议和基于http的协议。

目前先做protobuf 的二进制流协议。

协议头

```go
//同步协议的报文头
type SyncProtocolHead struct {
    //body 长度(除开这2个字节的长度)
    bodyLen uint16
    //im的账号id
    imuid int64
    //命令号
    cmdid int16
    //序列号
    seq int32
}
```

消息结构如下

![](/assets/msgStruct.png)

head 就是上面定义的固定长度的 SyncProtocolHead



