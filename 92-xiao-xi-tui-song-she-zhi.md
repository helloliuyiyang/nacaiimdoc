## 9.2 消息推送设置

关闭推送：[https://dev-otc.gac.top/v1/api/q/nacaiim/closePush](https://dev-otc.gac.top/v1/api/q/nacaiim/closePush)

开启推送：[https://dev-otc.gac.top/v1/api/q/nacaiim/openPush](https://dev-otc.gac.top/v1/api/q/nacaiim/openPush)

请求

```
请求参数：uid(int)
{
 "uid": 101
}
```

回应

```
{
    "code": 200,
    "message": "OK",
    "errorNo": 200,
    "msgDebug": "OK",
    "transNo": "",
    "data": {
        "result": "close push success"
    }
}

```



