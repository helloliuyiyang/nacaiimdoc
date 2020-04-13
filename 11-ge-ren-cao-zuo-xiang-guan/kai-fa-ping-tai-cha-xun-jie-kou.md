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

    type DappLinkReq struct {
        Dappid string `json:"dappid"`
        //起始页
        StartPage int `json:"start_page"`
        //每页的条数
        PageNum int `json:"page_num"`
    }

返回值

    type DappLink struct {
        //群/用户头像
        Avatar string `json:"avatar"`
        //群名/用户昵称
        Nickname string `json:"nickname"`
        //关联时间
        RelatedTime int64 `json:"related_time"`
    }

    type DappidLinkRes struct {
        Dappid string `json:"dappid"`
        //起始页
        StartPage int `json:"start_page"`
        //每页的条数
        PageNum int `json:"page_num"`
        Links []DappLink `json:"links"`
    }



