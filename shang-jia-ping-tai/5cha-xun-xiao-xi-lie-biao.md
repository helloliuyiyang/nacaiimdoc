### 查询消息列表

###### json结构：

```
{
    "api_name":"select_im_group_db,
    "repair_bill":"string",
    "max_line":1
}
```

信息字段含义：

| 字段 | 含义 |
| :--- | :--- |
| api\_name | 调用API名称 |
| repair\_bill | 工单号 |
| max\_line | 当前记录条数 |

回应消息

```
{
    "api_name":"set_im_user_no,
    "code":200,
    "MaxLine":1,
    “desp”：info
}
```

回应消息api\_name 代表当前调用的那个函数。

code代表这个消息的调用结果。200 为成功

desp是返回的消息。消息json见 给前端通知聊天消息

