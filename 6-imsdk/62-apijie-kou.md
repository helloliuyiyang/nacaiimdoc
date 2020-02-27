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

这2个函数的区别是IMSendPeeerMsg 发送消息时，不指定标志位。标志位为0.

IMSendPeeerMsgWithFlag 发送消息时，可指定标志位,目前的标志位只有1个。

msgflag=1 代表需要进行好友验证。

当是给订单的承兑人等不需要进行好友校验的消息，请使用IMSendPeeerMsgWithFlag   msgflag 为0 或者IMSendPeeerMsg 的函数调用发送。

当是给好友发送时，请使用IMSendPeeerMsgWithFlag msgflag=1  进行发送。



