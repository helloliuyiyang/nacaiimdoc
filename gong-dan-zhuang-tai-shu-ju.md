工单状态数据

    type DBOrderStatus struct {
    	Orderid string `json:"orderid" xorm:"orderid pk char(24) notnull unique"`
    	//这个订单的状态
    	OrderStatus int `json:"order_status" xorm:"order_status index"`
    	//上一个状态
    	PreOrderStatus int `json:"pre_order_status" xorm:"pre_order_status"`
    	//当前状态的时间戳-30
    	StatusTime int64 `json:"status_time" xorm:"status_time"`
    }



