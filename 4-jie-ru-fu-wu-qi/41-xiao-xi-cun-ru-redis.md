## 4.1 消息存入redis

聊天消息在redis中使用ZSET 存储。分数使用每个消息的msgid,msgid是全局的编号，用来查找消息。  
点对点的zsetkey为: impeer_msg:userid_

群组的zsetkey为:imgroup_msg:groupid_



点对点消息的一个用户使用一个ZSET保存他的点对点的消息。

一个群组使用一个ZSET保存他的的群组消息。

