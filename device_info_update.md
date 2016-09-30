# 设备信息更改

AIOT开放API可供第三方应用更改设备基本信息，如设备类型、设备名称等。

| **API** | /open/device/info/upload |
| --: | :-- |
| **描述** | 更新设备信息 |
| **header** | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} |
| **payload** | {"openId":"xxx","**did**":"xxx","**data**":{"name": "xxx", "firmwareVersion": "xxx", "model":"xxx", "chipVersion":"xxx", "longitude":"xxx", "latitude":"xxx","chipVersion":"xxx",...}} |
| **response** | {"code":0(errorcode), "result":"msg"}} |

> 只需要在data中填写要更改的信息的值。



