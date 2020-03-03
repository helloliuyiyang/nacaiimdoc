### 6.2.6 日志接口

```
//：上报日志
func AppLogsDebug(template string, v ...interface{}) {

	logs.Debug(template, v...)
}

func AppLogsTrace(template string, v ...interface{}) {

	logs.Trace(template, v...)
}

func AppLogsInfo(template string, v ...interface{}) {

	logs.Info(template, v...)
}

func AppLogsWarn(template string, v ...interface{}) {

	logs.Warn(template, v...)
}

func AppLogsError(template string, v ...interface{}) {

	logs.Error(template, v...)
}
func AppLogsFatal(template string, v ...interface{}) {

	logs.Fatal(template, v...)
}
```



