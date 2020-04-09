### **2.获取个人dapp**

所属服务：qim

提供对象：钱包app

开发者：devil

报错频率：

URL

```
/nacaiim/getUserDappids
```

请求参数

    type GetUserDappidsReq struct {
       Uid  uint64 `json:"uid"`
    }

返回值

    type GetUserDappidsRes struct {
       Uid  uint64 `json:"uid"`
       Dappids []string `json:"dappids"`
    }



