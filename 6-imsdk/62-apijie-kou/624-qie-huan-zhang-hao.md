### 6.2.4  切换账号

```
//3.2  修改账号
func IMSdkChangeNo(newNo string, passwd string, Uid int64) bool
```

切换账号 这个函数必须在上次启动成功后，才能调用这个函数。上次如果没启动成功，请调用SetImUserNo这个函数。



