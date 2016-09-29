# 设备在线离线


AIOT通过心跳包时刻监听设备的在线离线状态，AIOT将设备的在线离线消息开放给第三方应用，通过推送的方式进行。需要第三方应用后台提供接口，消息推送的格式如下：

| payload | header | 描述 |
| -- | -- | -- |
| {"did":"xxx","state":0-online/1-offline} | {"Appid":"xxx","Appkey":"xxx"} | 心跳推送 |

> - did: 设备id
> - timeStamp: 心跳包的时间戳，单位为s
> - Appid: 第三方应用的appId
> - Appkey: 第三方应用的appKey