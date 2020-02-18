### 6.2.3 获取当前服务端的配置信息

```
IMSdkGetServerNodeInfo
```

这个函数调用返回当前的服务端的配置信息。返回的是一个json的字符串，APP 把这个信息保存到数据库中去进行缓存。在下次客户端启动的时候，再传给SDK，就是由app 帮sdk进行缓存。

使用示例

    	strconfigInfoLocal := `{"confgiinfo":{"node_array":[{"id":1,"tcp_port":22983,"udp_port":22984,"weight":100,"server_type":1,"tcp_protocol":"\"\"","address":"154.197.26.25","disabled":0},{"id":2,"tcp_port":22985,"udp_port":22986,"weight":100,"server_type":2,"tcp_protocol":"\"\"","address":"154.197.26.25","disabled":0},{"id":3,"tcp_port":21983,"udp_port":21985,"weight":100,"server_type":1,"tcp_protocol":"\"\"","address":"52.183.46.177","disabled":0},{"id":4,"tcp_port":31983,"udp_port":31985,"weight":100,"server_type":2,"tcp_protocol":"\"\"","address":"52.183.46.177","disabled":0}]},"confgiinfo_timestamp":1582004741,"im_account_info_array":[{"no":"zxt77","uid":707}]}`

    	sdkv2.IMSdkSetBufferedServerNodeInfo(strconfigInfoLocal)

    	if !sdkv2.IMSdkStartup() {
    		return
    	}
    	strconfigInfo := sdkv2.IMSdkGetServerNodeInfo()
    	logs.Info("IMSdkGetServerNodeInfo strconfigInfo:%s", strconfigInfo)



