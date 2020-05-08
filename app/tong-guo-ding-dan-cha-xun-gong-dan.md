### 通过订单查询工单

所属服务：repair

提供对象：承兑app

开发者：cary

报错频率：

URL

```
/repair/appUser/getRepairId
```

请求参数

    type GetRepairIdReq struct {
        From    string `json:"from"`
        TradeId string `json:"tradeId"` //支付订单号
    }

返回值

    type GetRepairIdRes struct {
        Repairid string `json:"repairid"`//工单号
    }



