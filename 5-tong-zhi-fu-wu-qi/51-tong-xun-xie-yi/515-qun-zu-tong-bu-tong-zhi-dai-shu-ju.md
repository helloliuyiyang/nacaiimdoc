### 5.1.5 群组同步通知带数据

用户A 向群组发送消息,access\_server 收到消息，保存后，给群组里的每个用户发个更新通知，同时带上这条数据。

![](/assets/groupSyncNotifyWithData.png)

3:通知服务器给客户端的群组同步通知\(IM\_CMD\_GROUP\_NOTIFY\_SYNC\_HAS\_CHATDATA = 338\)

