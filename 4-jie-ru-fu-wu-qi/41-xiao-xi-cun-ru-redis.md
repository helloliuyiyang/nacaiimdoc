## 4.1 消息存入redis

聊天消息在redis中使用ZSET 存储。分数使用每个消息的msgid,msgid是全局的编号，用来查找消息。  
点对点的key为: im_chatmsg\_userid_

