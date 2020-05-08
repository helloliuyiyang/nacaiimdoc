### 用户申诉列表

所属服务：repair

提供对象：钱包app

开发者：cary

报错频率：

URL

```
/repair/appUser/queryRepairList
```

请求参数

    type UserAccountRepairBillQueryReq struct {
        From        string `json:"from"`
        CurrentPage int    `json:"currentPage"`
        PageSize    int    `json:"pageSize"`
    }

返回值

    //工单响应结构体
    type UserAccountRepairBillQueryRes struct {
        //总条数
        TotalRecordNum int64 `json:"total_record_num"`
        //开始位置
        StartPos int `json:"start_pos"`
        PageNum  int `json:"page_num"`
        //返回多少条数据
        PageTotalRecord int `json:"pageTotalRecord"`
        //共多少页
        TotalPage int                           `json:"totalPage"`
        Result    []WebUserAccountRepairBillRecord `json:"data"`
    }


    type WebUserAccountRepairBillRecord struct {
        BillStatus   string `json:"billStatusDesc"`
        BillType     string `json:"billTypeDesc"`
        CreateTime   string `json:"createTime"`
        RepairBillNo string `json:"repairBillNo"`
        SubName      string `json:"subName"`
        // 链账号
        SubmitUser string `json:"submitUser"`
        //青苹果账号名
        SubmitUserAccount string `json:"submitUserAccount"`

        TradeId    string `json:"tradeId"`
        UpdateTime string `json:"updateTime"`

        SubMitSubUser string `json:"submitSubUser"`
    }



