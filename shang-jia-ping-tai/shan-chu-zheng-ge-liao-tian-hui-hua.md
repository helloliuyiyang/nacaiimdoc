### 删除整个聊天会话

json结构：

```
{
    "api_name":"delete_from_groupid,
    "repair_bill":"string"
}
```

信息字段含义：

| 字段 | 含义 |
| :--- | :--- |
| api\_name | 调用API名称 |
| repair\_bill | 工单号 |

回应消息

```
{
    "api_name":"delete_from_groupid,
    "code":200,
    "desp":"OK"
}
```

回应消息api\_name 代表当前调用的那个函数。

code代表这个消息的调用结果。200 为成功

desp为调用失败，就是code 为非200 的描述信息。

