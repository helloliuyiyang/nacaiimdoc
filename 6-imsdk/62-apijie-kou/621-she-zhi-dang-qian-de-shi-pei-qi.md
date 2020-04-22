### 6.2.1 设置当前的网络适配器

```
//0:没有网络，1：WIFI 2:GPRS(移动网络)
//str_mobile_carriers  运营商的网络 中国电信:china_telecom 中国移动:china_mobile 中国联通:china_unicom
func SetNetworkCurMode(mode int,str_mobile_carriers string)
```

这个函数调用由app上层发生了WIFI，移动数据网络切换时，告诉底层SDK，网络发生了改变。可以让SDK 能快速的切换WIFI 或者4G。否则SDK 要等待30秒才能探测到发生了切换。不需要在sdk初始启动时设置。

```
    这个函数有2个参数，第一个参数表示当前的网络是WIFI 还是数据网络。第二个参数表示当前如果使用的是数据网络时，是那个
    运营商。当如果是WIFI 的时候，会忽略这个参数。
```

这个函数在启动APP 时候，需要调用这个函数，在后面进行网络切换时也要调用这个函数。在初始的时候，调用这个函数告诉当前

APP 使用的啥网络。

