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

    //obj对象属性,原web端返回的数据结构
    type AcceptorAppeal struct {
    	//工单状态
    	BillStatus int `json:"billStatus"`
    	//工单单号
    	RepairBillNo string `json:"repairBillNo"`
    	//im的最后更新时间
    	ImUpdateTime string `json:"imUpdateTime"`
    	//该工单留言的数量，用于在页面上展示用的
    	RepairBillMessageCount int `json:"repairBillMessageCount"`
    	//工单的会员名称
    	SubName string `json:"subName"`
    	//工单问题所属用户角色
    	UserRole int `json:"userRole"`
    }

回应消息api\_name 代表当前调用的那个函数。

code代表这个消息的调用结果。200 为成功

desp为调用失败，就是code 为非200 的描述信息。

