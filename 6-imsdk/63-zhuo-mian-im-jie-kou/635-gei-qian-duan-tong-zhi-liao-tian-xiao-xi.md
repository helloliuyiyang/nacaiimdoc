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
  int64     PreOffset=10;
  int64  toUID=11;
  bytes  content=12;
}
```

在IMSDK 中获取这个数据的地方是

```
//收到了群组的聊天消息
func OnImGroupChartEvent(data []byte) {

	var msg protoc.ImGroupSendMsgSync
	err := proto.Unmarshal(data, &msg)
	if err != nil {
		logs.Error("Unmarshal to [ImGroupSendMsgSync] error:%s", err)
		return
	}

	if msg.FromUID == selfUserID {
		//自己发送出去的消息
		logs.Error("OnImGroupChartEvent:me send chat msg:%s,offset:%d NextOffset:%d", msg.Content, msg.Offset, msg.NextOffset)
	} else {
		logs.Error("OnImGroupChartEvent:fromuid[%d] groupid[%d] received chat msg:%s",
			msg.FromUID, msg.ToGroupid,
			msg.Content)
	}
	sdkv2.IMAckGroupOffset(msg.GetToGroupid(), msg.Offset)

}
```



