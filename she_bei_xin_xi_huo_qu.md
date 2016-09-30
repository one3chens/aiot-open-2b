# 设备信息获取

AIOT开放API可供第三方应用查询设备基本信息，如设备id、设备类型、设备名称、固件版本等。

| **API** | /open/device/query |
| --: | -- |
| **描述** | 查询设备信息 |
| **header** | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} |
| **payload** | {"openId":"xxx","**did**":"xxx"} |
| **response** | {"code":0(errorcode), "result":{"did":"xxx", "model":"xxx", "name":"xxx", "firmwareVersion": "xxx", "state":"xxx", "chipVersion":"xxx", "longitude":"xxx", "latitude":"xxx"}}} |

| **API** | /open/device/query/option |
| --: | -- |
| **描述** | 查询设备特定信息 |
| **header** | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} |
| **payload** | {"openId":"xxx","**did**":"xxx","**option**":["option1","option2",...]} |
| **response** | {"code":0(errorcode), "result":{"did":"xxx", "option1":"xxx", "option2":"xxx", ...}} |

| **API** | /open/device/query/children |
| --: | -- |
| **描述** | 查询网关下子设备信息 |
| **header** | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} |
| **payload** | {"openId":"xxx","**did**":"xxx"} |
| **response** | {"code":0(errorcode), "result":[{"did":"xxx", "model":"xxx", "name":"xxx", "firmwareVersion": "xxx", "state":"xxx", "chipVersion":"xxx", "longitude":"xxx", "latitude":"xxx"}]}} |

| /open/device/query/children | 查询网关下子设备信息 | {"openId":"xxx","**did**":"xxx"} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0(errorcode), "result":[{"did":"xxx", "model":"xxx", "name":"xxx", "firmwareVersion": "xxx", "state":"xxx", "chipVersion":"xxx", "longitude":"xxx", "latitude":"xxx"}]}} |
| /open/device/query/children | 查询网关下子设备特定信息 | {"openId":"xxx","**did**":"xxx","**option**":["option1","option2",...]} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0(errorcode), "result":[{"did":"xxx", "option1":"xxx", "option2":"xxx", ...}]}} |
| /open/device/query/user | 查询用户所有设备的信息 | {"openId":"xxx"} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0(errorcode), "result":[{"did":"xxx", "model":"xxx", "name":"xxx", "firmwareVersion": "xxx", "state":"xxx", "chipVersion":"xxx", "longitude":"xxx", "latitude":"xxx"}{"did":"xxx", "model":"xxx", "name":"xxx", "firmwareVersion": "xxx", "state":"xxx", "chipVersion":"xxx", "longitude":"xxx", "latitude":"xxx"}]}} |

> - did: 设备id
> - openId: 用户id
> - Appid: 第三方应用appId
> - Appkey: 第三方应用appKey
> - Access-Token: 用户token
> - model: 设备类型
> - firmwareVersion: 设备固件版本
> - chipVersion: 设备芯片版本
> - state: 设备在线/离线状态，0-离线,1-在线
> - longitude, latitude: 设备所处经纬度
> - errorcode: 错误码，详见附件