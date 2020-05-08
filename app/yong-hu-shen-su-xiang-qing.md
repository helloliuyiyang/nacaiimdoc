### 用户申诉详情

所属服务：repair

提供对象：钱包app

开发者：cary

报错频率：

URL

```
/repair/appUser/queryRepairDetail
```

请求参数

    type AppUserRepairDetailReq struct {
    	From         string `json:"from"`
    	RepairBillNo string `json:"repairBillNo"`
    }

返回值

    type WebAppUserRepairBillDetailRes struct {
    	RepairBillNo       string                   `json:"repairBillNo"`
    	RepairBillType     string                   `json:"billTypeDesc"`
    	RepairBillStatus   string                   `json:"billStatusDesc"`
    	BillType           int                      `json:"billType"`
    	HandleRemark       string                   `json:"handleRemark"`
    	Content            string                   `json:"content"`
    	TradeId            string                   `json:"tradeId"`
    	SubName            string                   `json:"subName"`
    	AmountRmb          int64                    `json:"amountRmb"`
    	HandleImgs         []string                 `json:"handleImgs"`
    	RelativeImgUrlList []string                 `json:"relativeImgUrlList"`
    	CurAcceptorEos     string                   `json:"curAcceptorEos"`
    	Creator            string                   `json:"creator"`
    	Receiver           string                   `json:"receiver"`
    	PeerOrderNo        string                   `json:"peerOrderNo"`
    	CreateTime         string                   `json:"createTime"`
    	CreateTimestamp    int64                    `json:"create_timestamp"`
    	BillStatus         int                      `json:"billStatus"`
    	OrderStatus        string                   `json:"order_status"`
    	RepairBillLogList  []entity.DBRepairBillLog `json:"repairBillList"`
    	CreatorRole        int                      `json:"creatorRole"`
    	Groupid            int64                    `json:"groupid"`
    }



