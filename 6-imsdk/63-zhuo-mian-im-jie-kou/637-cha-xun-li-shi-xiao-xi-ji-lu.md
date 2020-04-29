### 查询历史消息记录

json结构：

```
{
    "api_name":"select_chat_list"
}
```

信息字段含义：

| 字段 | 含义 |
| :--- | :--- |
| api\_name | 调用API名称 |

回应消息

```
{
    "api_name":"select_chat_list,
    "code":200,
    "desp":info,
}
```

回应消息api\_name 代表当前调用的那个函数。

code代表这个消息的调用结果。200 为成功

desp是返回的info数组。消息json见 给前端通知聊天消息。



