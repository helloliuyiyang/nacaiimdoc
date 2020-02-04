### 8.1.3  发送群组聊天消息的回应

服务端向客户端发送群组的聊天消息的回应

chatsync\_server-&gt;imsdk

这个消息事件（IM\_CMD\_GROUP\_SEND\_IM\_RES = 329）这消息的pb为如下:

这个消息的PB 为

```js
message ImGroupSendMsgRes {
 Head head=1;
 int64 toGroupid=2;
 int32 len=3;
 int32 msgid=4;
 int32 code=5;
 int64 offset=6;
 string desp=7;

}
```

协议文件位置为gopath/src/nacaiim/protoc/msg.proto

这个消息对应在[8.1.2 发送群组的聊天消息 中](/812-fa-song-qun-zu-de-liao-tian-xiao-xi.md)的第5步。

| 字段 | 备注 | 可选 |
| :--- | :--- | :--- |
| head | 消息的头，这个版本里没有了 | 没有 |
| toGroupid | 接收这个消息的群组ID | 必须 |
| len | 消息长度 | 必须 |
| msgid | 服务端给客户端回应消息的msgid.就是客户端发送上来的ID | 必须 |
| code | 服务端对这个消息的回应。200为发送成功。非200 为不成功，404 群组不存在。 | 必须 |
| offset | 这个消息在服务端分配的偏移位置 | 必须 |
| desp | 这个消息发送失败的错误描述 | 可选 |



