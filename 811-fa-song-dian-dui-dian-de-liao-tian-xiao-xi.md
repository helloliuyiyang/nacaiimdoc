### 8.1.1  发送点对点的聊天消息

客户端向服务端发送点对点的聊天消息

imsdk-&gt;chatsync\_server

这个消息事件（IM\_CMD\_CLIENT\_SEND\_IM     = 315）这消息的pb为如下:

```go
//客户端向服务端发送聊天的消息 3.8
message ImClientSendMsg {
  Head head=1;
  int64  offset=2;
  int64  nextOffset=3;
  int64  fromUID=4;
  int64  toUID=5;
  int32  timestamp=6;
  int32  msgid=7;
  int32  len=8;
  int32  msgType=9;
  int32  msgFlag=10;
  int64  preOffset=11;
  bytes  content=12;
}
```

协议文件位置为gopath/src/nacaiim/protoc/msg.proto

| 字段 | 备注 | 可选 |
| :--- | :--- | :--- |
| head | 这个消息的头\(当前版本里不需要了\) | 没有 |
| offset | 这个消息的偏移。客户端发送上来的。这个字段没有意义。忽略 | 没有 |
| nextOffset | 这个消息的下一个偏移。客户端发送上来的。这个字段没有意义。忽略 | 没有 |
| fromUID | 发送消息的用户ID | 必须 |
| toUID | 接收消息的用户id | 必须 |
| timestamp | 发送这个消息的时间戳 | 必须 |
| msgid | 发送这个消息的客户端生成的msgid | 必须 |
| len | 发送的这个消息的长度 | 必须 |
| msgType | 发送的这个消息的类型 | 必须 |
| msgFlag | 发送的这个消息的标记 | 必须 |
| preOffset | 前一个消息的偏移。客户端发送上来的。这个字段没有意义。忽略 | 没有 |

![](/assets/chatmsgsync.png)

2：请求发送单聊消息到chatsync_server, 连接为tcp 或者quic协议的udp连接._

3:请丢发送单聊消息到access\_server  的请求是服务端的内部调用，需要为grpc调用。

5:请求发送单聊消息成功的回应消息（IM\_CMD\_CLIENT\_SEND\_IM\_RES = 316）这个消息的PB如下

```js
message ImClientSendMsgRes {
 Head head=1;
 int64 toUID=2;
 int32 len=3;
 int32 msgid=4;
 int32 code=5;
 int64 offset=6;
}
```

协议文件位置为gopath/src/nacaiim/protoc/msg.proto

