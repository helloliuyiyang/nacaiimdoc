## 9.1 消息推送协议

当用户不在线时，IM 通过极光推送服务将消息推送到APP。推送的协议带有下面几个扩展字段。

```js
    {
    "mt":"red_packet",
    "st":"redPacketSend",
    "gid":"11",
    "sync_offset":9001,
    "uid":90011,
    }
```

| 字段 | 备注 |
| :--- | :--- |
| mt | 推送的消息的主类型 |
| st | 推送的消息的子类型 |
| sync\_offset | 推送的消息的ID |
| uid | 这个推送的消息的接收的id |
| from\_uid | 这个推送消息的发送者的用户的uid |

消息分类有下面几个分类对应mt

| 消息主类型 | 子类型列表 | 备注 |
| :--- | :--- | :--- |
| trading\_msg |  coin\_trading,entrust\_order,entrust | 币币 |
| red\_packet |  redPacketSend,redPacketReceived,redPacketRefund | 红包 |
| funding\_status\_changed | 无 | 订单消息 |
| repair\_bill\_im |  无 | 工单消息 |
| chat\_msg | 无 | 聊天消息 |



