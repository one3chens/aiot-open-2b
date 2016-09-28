# 设备信息获取

AIOT开放API可供第三方应用查询设备基本信息，如设备id、设备类型、设备名称等。

| API | 描述 | payload | header | response |
| -- | -- | -- | -- | -- |
| /open/device/query | 查询设备信息 | {"openId":"xxx","did":"xxx"} | {"Appid":"xxx","Appkey":"xxx","Openid":"xxx","Access-Token":"xxx"} | {"code":0|errorcode, "result":{"did":"value", "model":"value", "name":"value"}}} |
| /open/device/query/user | 查询用户所有设备的信息 | {"openId":"xxx"} | {"Appid":"xxx","Appkey":"xxx","Openid":"xxx","Access-Token":"xxx"} | {"code":0|errorcode, "result":[{"did":"value", "model":"value", "name":"value"}{"did":"value", "model":"value", "name":"value"}]}} |