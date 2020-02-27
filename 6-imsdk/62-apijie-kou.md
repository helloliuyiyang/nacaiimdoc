### 6.2.5 发送点对点消息

有下面的函数调用

```
func IMSendPeeerMsg(appmsgID int32, recvUID int64, msgType int64, msgLen int64, data []byte) bool 
```

和

```
//13.1:发送点对点的消息指定标记位
func IMSendPeeerMsgWithFlag(appmsgID int32, recvUID int64, msgType int64, msgflag int64, msgLen int64,
 data []byte) bool {
```



