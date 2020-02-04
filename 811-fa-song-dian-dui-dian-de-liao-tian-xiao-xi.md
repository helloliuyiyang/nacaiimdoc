### 8.1.1  发送点对点的聊天消息

客户端向服务端发送点对点的聊天消息

这个消息的pb为

```go
//客户端向服务端发送聊天的消息 3.8
message ImClientSendMsg {
  Head head=1;
  int64  offset=2;
  int64  nextOffset=3;
  int64  fromUID=4;
  int64  toUID=5;
  int32  timestamp=6;
  int32  msgid=7;
  int32  len=8;
  int32  msgType=9;
  int32  msgFlag=10;
  int64  preOffset=11;
  bytes  content=12;
}
```


