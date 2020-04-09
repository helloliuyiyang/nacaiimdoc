### **2.操作群dapp**

所属服务：qim

提供对象：钱包app

开发者：devil

报错频率：

URL

```
/nacaiim/GroupDappidOp
```

请求参数

    type GroupDappidOpReq struct {
       Uid     int64 `json:"uid"`
       Groupid int64 `json:"groupid"`
       Op int `json:"op"` //1:添加 2:删除
       Dappid  string `json:"dappid"` //操作对象
    }

返回值

    type GroupDappidOpRes struct {
       Groupid int64 `json:"groupid"`
       Op int `json:"op"` //1:添加 2:删除
       Dappid string `json:"dappid"` //操作对象
       Dappids  []string `json:"dappids"` //修改后结果
    }



