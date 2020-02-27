### 6.2.5 发送点对点的消息

调用的API

```
func IMSendPeeerMsg(appmsgID int32, recvUID int64, msgType int64, msgLen int64, data []byte) bool {
```

和

```
func IMSendPeeerMsgWithFlag(appmsgID int32, recvUID int64, msgType int64, msgflag int64, 
msgLen int64, data []byte) bool
```

这2个函数的区别是IMSendPeeerMsgWithFlag 带了msgflag,发送消息的时候可指定msgflag，指定为1 就代表需要发送消息进行好友验证。为0不需要好友验证。

IMSendPeeerMsg 是发送消息时不需要好友验证。例如用于给承兑人发消息。



