### **承兑人申诉详情**

json结构：

```
{
    "api_name":"acceptor_appeal_detail,
    "id":1

}
```

信息字段含义：

| 字段 | 含义 |
| :--- | :--- |
| api\_name | 调用API名称 |
| id | 数据库主键ID |

回应消息

```
{
    "api_name":"acceptor_appeal_detail,
    "code":200,
    "data":obj,
    "desp":""

}
```

```
//obj对象属性,原web端返回的数据结构
{
    "order_no":"申诉号",
    "type":"申诉类型",
    "status":"申诉状态"
    ...
}
```

回应消息api\_name 代表当前调用的那个函数。

code代表这个消息的调用结果。200 为成功

desp为调用失败，就是code 为非200 的描述信息。

