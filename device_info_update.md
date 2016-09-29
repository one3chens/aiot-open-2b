# 设备信息更改

AIOT开放API可供第三方应用更改设备基本信息，如设备类型、设备名称等。

| API | 描述 | payload | header | response |
| -- | -- | -- | -- | -- |
| /open/device/info/upload | 更新设备信息 | {"openId":"xxx","**did**":"xxx","**data**":{"name": "value", "firmwareVersion": "value", "model":"value", "chipVersion":"value", "longitude":"value", "latitude":"value","chipVersion"...}} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0(errorcode), "result":"msg"}} |

> 需要更改设备的某个信息，只需要在data中填写该信息的值