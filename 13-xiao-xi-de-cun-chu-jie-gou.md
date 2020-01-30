## 1.3 消息的存储结构

![](/assets/chatMsgStorageStruct.png)

上图是一个用户的消息的存储结构，pre-msgid  都是指向上一个消息的msgid,类似一个单链表的存储。

offset是一个递增的序列，上图代表这个用户1，2，3的3条连续消息的结构.



