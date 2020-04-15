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

    //使用token 

    //不使用废弃直接使用token验证身份

    type UserDappidOpReq struct {
       Op int8 `json:"op"` //1:添加 2:删除
       Dappid string `json:"dappid"` //操作对象
    }

返回值

    type DappInfo struct {
        //dapp的id
        Id string `json:"id"`
        //logo图片
        Logo string `json:"logo"`
        //dapp的名字
        Name string `json:"name"`
        //简介
        Introduction string `json:"introduction"`
        //网站入口
        WebEntrance string `json:"web_entrance"`
        //关联状态 1为开启了关联功能 0为关闭了关联功能
        RelateStatus int `json:"relate_status"`

        //上下架 1.上架 0.下架
        Status int `json:"status"`
    }




    type UserDappidOpRes struct {
        Op int `json:"op"` //1:添加 2:删除
        Dappid string `json:"dappid"`
        Dapps  []DappInfo `json:"dapps"`
    }



