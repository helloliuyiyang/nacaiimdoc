### 6.1.1 v2版本聊天消息解析

v2版本改动了客户端收到的聊天消息的格式。

对应的文件为protoc/Sync.java

之前用的文件为protoc/Msg.java

点对点的（IM\_CMD\_CLIENT\_SEND\_IM=315\)

```js
message ImClientSendMsgSync {

  int64  offset=1;
  int64  nextOffset=2;
  int64  fromUID=3;
  int64  toUID=4;
  int32  timestamp=5;
  int32  msgid=6;
  int32  len=7;
  int32  msgType=8;
  int32  msgFlag=9;
  int64  preOffset=10;
  bytes  content=11;
}
```

群组的\(IM\_CMD\_GROUP\_SEND\_IM=328\)

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
  int64     PreOffset=10;
  int64  toUID=11;
  bytes  content=12;
}
```



