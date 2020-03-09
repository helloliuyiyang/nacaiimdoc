### 6.3.5 给前端通知聊天消息

IMSDK 收到消息后，通过WEBSOCKET 将聊天的数据消息转发给前端。

使用json格式

```js
message ImGroupSendMsgSync {
  int64  offset=1;
  int64  nextOffset=2;
  int64  fromUID=3;
  int64  toGroupid=4;
  int32  timestamp=5;
  int32  msgid=6;
  int32  len=7;
  int32  msgType=8;
  int32  msgFlag=9;
  int64	 PreOffset=10;
  int64  toUID=11;
  bytes  content=12;
}
```



