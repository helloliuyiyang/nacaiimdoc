### **2.开放平台获取dapp关联列表**

所属服务：qim

提供对象：钱包app

开发者：devil

报错频率：

URL

```
/nacaiim/getDappidLink
```

请求参数

    type GetDappLinkReq struct {
       Dappid  string `json:"dappid"`
    }

返回值

    type GetDappLinkRes struct {
       Dappid  string `json:"dappid"`
       Dappids []string `json:"dappids"`
       //logo name link name (db or api)
    }



