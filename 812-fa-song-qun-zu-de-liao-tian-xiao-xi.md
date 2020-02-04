## 8.1.2 发送群组的聊天消息

客户端向服务端发送群组的聊天消息。

imsdk-&gt;chatsync\_server

这个消息事件（IM\_CMD\_GROUP\_SEND\_IM     = 328）这消息的pb为如下:

这个消息的PB 为

```go
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

协议文件位置为gopath/src/nacaiim/protoc/msg.proto

| 字段 | 备注 | 可选 |
| :--- | :--- | :--- |
| head | 这个消息的头（这个版本不需要了\) | 没有 |
| offset | 这个消息的偏移,客户端发送上去的，没有这个字段 | 没有 |
| nextOffset | 这个消息的下个消息的偏移，客户端发送上去的，没有这个字段 | 没有 |
| fromUID | 发送消息的用户id | 必须 |
| toGroupid | 接收消息的群组id | 必须 |
| timestamp | 发送这个消息时的时间戳 | 必须 |
| msgid | 发送这个消息的消息id | 必须 |
| len | 发送这个消息的长度 | 必须 |
| msgType | 发送的这个消息的类型 | 必须 |
| msgFlag | 发送的这个消息的标记 | 必须 |
| PreOffset | 发送这个消息的前一个的偏移，客户端发送上去的。没有这个字段 | 没有 |
| content | 发送的这个消息的内容 | 必须 |

这个消息的交互流程

![](/assets/groupmsgsync.png)

