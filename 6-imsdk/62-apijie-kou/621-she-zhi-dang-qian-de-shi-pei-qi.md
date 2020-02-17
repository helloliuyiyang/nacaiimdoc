### 6.2.1 设置当前的网络适配器

```
//0:没有网络，1：WIFI 2:GPRS(移动网络)
func SetNetworkCurMode(mode int)
```

这个函数调用由app上层发生了WIFI，移动数据网络切换时，告诉底层SDK，网络发生了改变。



