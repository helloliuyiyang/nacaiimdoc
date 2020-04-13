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
    }

    type UserDappidOpRes struct {
    	Groupid int64 `json:"groupid"`
    	Op int `json:"op"` //1:添加 2:删除
    	Dappid string `json:"dappid"`
    	Dapps  []DappInfo `json:"dapps"`
    }





