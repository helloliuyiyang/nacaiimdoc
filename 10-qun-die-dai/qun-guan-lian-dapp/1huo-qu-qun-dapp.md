### **2.获取群dapp**

所属服务：qim

提供对象：钱包app

开发者：devil

报错频率：

URL

```
/nacaiim/getGroupDappids
```

请求参数

    type GetGroupDappidsReq struct {
       Groupid int64 `json:"groupid"`
    }

返回值

    type GetGroupDappidsRes struct {
       Groupid int64 `json:"groupid"`
       Dappids  []string `json:"dappids"`
       //logo name link name (db or api)
    }



