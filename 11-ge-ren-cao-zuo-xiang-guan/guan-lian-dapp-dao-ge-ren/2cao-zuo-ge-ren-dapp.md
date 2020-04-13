### **2.操作个人dapp**

所属服务：qim

提供对象：钱包app

开发者：devil

报错频率：

URL

```
/nacaiim/UserDappidOp
```

请求参数

    type UserDappidOpReq struct {
       Uid  uint64 `json:"uid"`
       Op int8 `json:"op"` //1:添加 2:删除
       Dappid string `json:"dappid"` //操作对象
    }

返回值

    type GetUserDappidOpRes struct {
       Uid  uint64 `json:"uid"`
       Op int8 `json:"op"` //1:添加 2:删除
       Dappid string `json:"dappid"` //操作对象
       Dappids []string `json:"dappids"`
       //logo name link name (db or api)
    }



