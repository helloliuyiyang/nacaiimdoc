### 6.2.2  设置当前缓存的服务端的配置信息

```
func IMSdkSetBufferedServerNodeInfo(configInfo string) bool {
```

因为客户端连接的网络是AWS 网络，这个网络很差，HTTP 有时请求不到服务端的配置信息。

客户端成功从获取到IM 的服务端的配置信息后，把这个信息保存到数据库中。这个信息是一个json的字符串。示例如下

```js
{
    "confgiinfo":{
        "node_array":[
            {
                "id":1,
                "tcp_port":22983,
                "udp_port":22984,
                "weight":100,
                "server_type":1,
                "tcp_protocol":"""",
                "address":"154.197.26.25",
                "disabled":0
            },
            {
                "id":2,
                "tcp_port":22985,
                "udp_port":22986,
                "weight":100,
                "server_type":2,
                "tcp_protocol":"""",
                "address":"154.197.26.25",
                "disabled":0
            },
            {
                "id":3,
                "tcp_port":21983,
                "udp_port":21985,
                "weight":100,
                "server_type":1,
                "tcp_protocol":"""",
                "address":"52.183.46.177",
                "disabled":0
            },
            {
                "id":4,
                "tcp_port":31983,
                "udp_port":31985,
                "weight":100,
                "server_type":2,
                "tcp_protocol":"""",
                "address":"52.183.46.177",
                "disabled":0
            }
        ]
    },
    "confgiinfo_timestamp":1582004741,
    "im_account_info_array":[
        {
            "no":"zxt77",
            "uid":707
        }
    ]
}
```



