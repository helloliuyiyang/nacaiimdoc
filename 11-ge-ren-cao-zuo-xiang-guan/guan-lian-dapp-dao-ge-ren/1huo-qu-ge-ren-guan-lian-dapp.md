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

        //状态 1代表创建未提交审核 2代表提交审核(审核中) 3代表审核通过(已上架) 4代表审核未通过 5代表已下架 6代表已删除
        Status int `xorm:"status"`
        //关联状态 1为开启了关联功能 0为关闭了关联功能
        RelateStatus int `json:"relate_status"
    }






    type GetUserDappidsRes struct {
       Uid  uint64 `json:"uid"`
       Dapps  []DappInfo `json:"dapps"`
    }



