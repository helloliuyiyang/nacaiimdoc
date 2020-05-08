### 承兑人申诉详情

所属服务：repair

提供对象：钱包app

开发者：cary

报错频率：

URL

```
/repair/appAccepter/queryAppRepairDetail
```

请求参数

    type AppDetailReq struct {
    	From         string `json:"from"`
    	RepairBillNo string `json:"repairBillNo"`
    }

返回值

    type Order struct {
    	//工单ID
    	Orderid  string `json:"repair_bill_no" xorm:"repair_bill_no pk char(24) notnull"` //工单号
    	BillType int    `json:"bill_type" xorm:"bill_type"`

    	HandleImgs   string `json:"handle_imgs" xorm:"handle_imgs"`       //处理图片
    	HandleRemark string `json:"handle_remark" xorm:"handle_remark"`   //处理结果
    	Priority     int    `json:"priority" xorm:"priority"`             //优先级
    	CreateTime   int64  `json:"create_time" xorm:"create_time index"` //创建时间 notnull

    	//工单受理读取标志
    	ReceiverRead int `json:"receiver_read" xorm:"receiver_read"`

    	Content   string `json:"content" xorm:"content"`       //工单内容
    	ImagesUrl string `json:"images_url" xorm:"images_url"` //图片相对路径

    	TradeId       string `json:"trade_id" xorm:"trade_id index"`             //订单号
    	RepairTradeId string `json:"repairTradeId" xorm:"repair_trade_id"` //补单号
    	AmountRmb     int64  `json:"amount_rmb" xorm:"amount_rmb"`         //充值金额
    	CreatorRead   int    `json:"creator_read" xorm:"creator_read"`     //工单发起人读取标志

    	AllocationTime int64 `json:"allocation_time" xorm:"allocation_time"`   //工单分配客服时间
    	FinishedTime   int64 `json:"finished_time" xorm:"finished_time index"` //工单完结时间
    	UpdateTime     int64 `json:"update_time" xorm:"update_time"`           //更新时间
    	//收款账户
    	PayeeAccount string `json:"payee_account" xorm:"payee_account"`
    	//工单完结原因
    	FinishReason string `json:"finish_reason"  xorm:"finish_reason"`

    	//这个工单原始订单的类型
    	OrderType int `json:"order_type" xorm:"order_type index"`
    	//工单状态
    	Bill_status int `json:"bill_status" xorm:"bill_status index"`
    	//------------------------------------------------
    	//工单发起人链账号
    	CreatorEos string `json:"creator_eos" xorm:"creator_eos"`
    	//工单发起人的子账号
    	CreatorSub      string `json:"creator_sub" xorm:"creator_sub"`
    	CreatorAccount  string `json:"creator_account" xorm:"creator_account"`   //工单发起人
    	CreatorNickname string `json:"creator_nickname" xorm:"creator_nickname"` //工单发起人名称
    	CreatorRole     int    `json:"creator_role" xorm:"creator_role"`         //工单发起人角色
    	//----------------------------------------------
    	//to
    	ReceiverAccount  string `json:"receiver_account" xorm:"receiver_account index"` //工单受理人账号
    	ReceiverNickname string `json:"receiver_nickname" xorm:"receiver_nickname"`     //工单受理人昵称
    	//工单受理人链账号(这个基本上没有链账号)
    	ReceiverEos string `json:"receiver_eos" xorm:"receiver_eos"`
    	//------------------------------------------------------
    	UserRole int    `json:"user_role" xorm:"user_role"` //问题所属角色
    	UserName string `json:"user_name" xorm:"user_name"` //问题所属账号名
    	UserEOS  string `json:"user_eos" xorm:"user_eos"`   //问题所属账号EOS名
    	//子账号
    	SubName string `json:"sub_name" xorm:"sub_name"`
    	//会员名
    	SubMember string `json:"sub_member" xorm:"sub_member"`
    	//---------------------------------------------------------
    	//这个工单参与的另一个人 角色
    	JoinUserRole int `json:"join_user_role" xorm:"join_user_role"`
    	//这个工单参与的另一个人 账号
    	JoinUserName string `json:"join_user_name" xorm:"join_user_name"`
    	//这个工单参与的另一个人 EOS账号
    	JoinUserEOS string `json:"join_user_eos" xorm:"join_user_eos"`
    	//这个工单参与的另一个人子账号
    	JoinSubName string `json:"join_sub_name" xorm:"join_sub_name"`
    	//--------------------------------------------------------------
    	//这个工单参与的 普通用户 角色
    	JoinUserAccountRole int `json:"join_user_account_role" xorm:"join_user_account_role"`
    	//这个工单参与的 普通用户工单 账号
    	JoinUserAccountName string `json:"join_user_account_name" xorm:"join_user_account_name"`
    	//这个工单参与的 普通用户的 EOS账号
    	JoinUserAccountEOS string `json:"join_user_account_eos" xorm:"join_user_account_eos"`
    	//--------------------------------------------------------------
    	Eosno string `json:"eosno" xorm:"eosno char(24) notnull index"`
    	//子账号
    	FromSubNo string `json:"from_sub_no" xorm:"from_sub_no"`
    	//执行这个单时这个用户的角色
    	From_user_role int `json:"from_user_role" xorm:"from_user_role"`
    	//订单的对端用户
    	To_no string `json:"to_no" xorm:"to_no char(24) notnull index"`
    	//对端用户的角色
    	To_no_role int `json:"to_no_role" xorm:"to_no_role"`
    	//关联的单号
    	PeerOrderNo string `json:"peer_order_no" xorm:"peer_order_no char(24) notnull"`
    	//补单的原订单id
    	RepairOriginOrderid string `json:"repair_origin_orderid" xorm:"repair_origin_orderid char(24) notnull default ''"`
    	//------------------------------------------------------------------------
    	//from的账号
    	FromAccount string `json:"from_account" xorm:"from_account index"`
    	//to的账号
    	ToAccount string `json:"to_account" xorm:"to_account index"`
    	//----------------------------------------------------------------------
    	//当前工单的商家
    	CurMerchjant string `json:"cur_merchant" xorm:"cur_merchant index"`
    	//当前工单的商家的子账号
    	CurMerchjantSub string `json:"cur_merchant_sub" xorm:"cur_merchant_sub index"`
    	//当前商家是否已经进入会话标记
    	CurMerchantJoinFlag int `json:"cur_merchant_join_flag" xorm:"cur_merchant_join_flag"`
    	//当前工单的承兑人
    	CurAccepter string `json:"cur_acceptor" xorm:"cur_acceptor index"`
    	//当前工单的普通用户
    	UserAccount string `json:"user_account" xorm:"user_account"`
    	//群组id
    	Groupid int64 `json:"groupid" xorm:"groupid"`
    	//app创建工单:1
    	IsApp int64 `json:"is_app" xorm:"is_app notnull default 0"`
    }



