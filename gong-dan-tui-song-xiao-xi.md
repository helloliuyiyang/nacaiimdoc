### 工单推送消息

工单推送如下数据

    type NotifyRepairStatus struct {
        //消息类型字符串
        MsgType      string               `json:"msg_type"`
        //接收这个消息的链账号
        Eosno        string               `json:"eosno"`
        //工单信息
        Order        *Order               `json:"order"`
        //工单状态信息
        OrderStatus  *DBOrderStatus       `json:"order_status"`
    }


MsgType 为repair\_status\_changed 表示工单状态改变了

这个json消息包含2个对象Order 工单对象，OrderStatus 工单的状态对象

这个消息和订单类似

对应IM 的消息类型为1001代表工单消息。


    type ImGroupSendMsgSync struct {
    	//本消息的同步key
    	Offset int64 `protobuf:"varint,1,opt,name=offset,proto3" json:"offset,omitempty"`
    	//下一个消息的同步key
    	NextOffset int64 `protobuf:"varint,2,opt,name=nextOffset,proto3" json:"nextOffset,omitempty"`
    	FromUID    int64 `protobuf:"varint,3,opt,name=fromUID,proto3" json:"fromUID,omitempty"`
    	ToGroupid  int64 `protobuf:"varint,4,opt,name=toGroupid,proto3" json:"toGroupid,omitempty"`
    	Timestamp  int32 `protobuf:"varint,5,opt,name=timestamp,proto3" json:"timestamp,omitempty"`
    	//消息序列号顺序递增的
    	Msgid   int32 `protobuf:"varint,6,opt,name=msgid,proto3" json:"msgid,omitempty"`
    	Len     int32 `protobuf:"varint,7,opt,name=len,proto3" json:"len,omitempty"`
    	MsgType int32 `protobuf:"varint,8,opt,name=msgType,proto3" json:"msgType,omitempty"`
    	MsgFlag int32 `protobuf:"varint,9,opt,name=msgFlag,proto3" json:"msgFlag,omitempty"`
    	//前一个同步key
    	PreOffset   int64  `protobuf:"varint,10,opt,name=PreOffset,proto3" json:"PreOffset,omitempty"`
    	ToUID       int64  `protobuf:"varint,11,opt,name=toUID,proto3" json:"toUID,omitempty"`
    	Content     []byte `protobuf:"bytes,12,opt,name=content,proto3" json:"content,omitempty"`
    	AppId       int32  `protobuf:"varint,13,opt,name=AppId,proto3" json:"AppId,omitempty"`
    	ContentIsPB int32  `protobuf:"varint,14,opt,name=contentIsPB,proto3" json:"contentIsPB,omitempty"`
    	//这个聊天消息的序列号
    	ChatSeq int32 `protobuf:"varint,15,opt,name=chatSeq,proto3" json:"chatSeq,omitempty"`
    	//这个聊天消息的端点号
    	Endpoint string `protobuf:"bytes,16,opt,name=endpoint,proto3" json:"endpoint,omitempty"`
    	//客户端确认的连续的消息序列号
    	AckChatSeq int32 `protobuf:"varint,17,opt,name=ackChatSeq,proto3" json:"ackChatSeq,omitempty"`
    	//这个消息分配的唯一ID
    	MsgUUID              int64    `protobuf:"varint,18,opt,name=msgUUID,proto3" json:"msgUUID,omitempty"`
    	XXX_NoUnkeyedLiteral struct{} `json:"-"`
    	XXX_unrecognized     []byte   `json:"-"`
    	XXX_sizecache        int32    `json:"-"`
    }






