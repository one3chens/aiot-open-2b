# 设备信息推送

当设备信息发生更改时，比如固件版本发生更改时，AIOT会及时将设备信息推送至第三方应用，需要第三方应用后台提供接口，这里定义推送的数据格式。

| msgType | device_resource |
| --: | -- |
| **描述** | 设备信息推送 |
| **header** | {"**Appid**":"xxx","**Appkey**":"xxx"} |
| **payload** | {"**msgType**":"device_resource","**did**":"xxx","**time**":xxx,"**data**":{"attr1":"xxx","attr2":"xxx",...}} |

| payload | header | 描述 |
| -- | -- | --- |
| {"msgType":"device_info","**did**":"xxx","**data**":{"mac": "xxx", "name": "xxx", "firmwareVersion": "xxx", "state":"xxx", "model":"xxx", "chipVersion":"xxx","longitude":"xxx", "latitude":"xxx"}} | {"Appid":"xxx","Appkey":"xxx"} | 设备信息推送 |

> - did: 设备id
> - msgType: 消息类型
> - state: 设备在线/离线状态，0-在线，1-离线
> - Appid: 第三方应用的appId
> - Appkey: 第三方应用的appKey