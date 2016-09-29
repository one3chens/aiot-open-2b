# 设备信息更改

AIOT开放API可供第三方应用更改设备基本信息，如设备类型、设备名称等。

| API | 描述 | payload | header | response |
| -- | -- | -- | -- | -- |
| /open/dev/info/upload | 更新设备信息 | {"openId":"xxx","**did**":"xxx","**data**":{"name": "value", "firmwareVersion": "value", "model":"value", "chipVersion":"value", "longitude":"value", "latitude":"value","chipVersion"...}} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0(errorcode), "result":"msg"}} |

| /open/device/query/user | 查询用户所有设备的信息 | {"openId":"xxx"} | {"Appid":"xxx","Appkey":"xxx","Openid":"xxx","Access-Token":"xxx"} | {"code":0(errorcode), "result":[{"did":"value", "model":"value", "name":"value"}{"did":"value", "model":"value", "name":"value"}]}} |