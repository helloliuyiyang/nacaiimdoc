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



