## 8.1.2 发送群组的聊天消息

客户端向服务端发送群组的聊天消息。

这个消息的PB 为

```js
message ImGroupSendMsg {
  Head head=1;
  int64  offset=2;
  int64  nextOffset=3;
  int64  fromUID=4;
  int64  toGroupid=5;
  int32  timestamp=6;
  int32  msgid=7;
  int32  len=8;
  int32  msgType=9;
  int32  msgFlag=10;
  int64     PreOffset=11;
  bytes  content=12;
}
```



