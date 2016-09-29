# 设备属性获取

AIOT开放API可供第三方应用查询设备属性。

| API | 描述 | payload | header | response |
| -- | -- | -- | -- | -- |
| /open/resource/query | 查询设备有哪些资源 | {"openId":"xxx","**did**":"xxx"} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0|errorcode, "result":{"did":"xxx","attr":[{"attr1":"xxx","name":"xxx","minValue":"xxx","maxValue":"xxx","enum":[xx,xx,xx]}]}} |
| /open/res/query/option | 查询设备的某些资源当前值 | {"openId":"xxx","**did**":"xxx","**option**":["attr1","attr2",...]} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0(errorcode), "result":{"did":"xxx","data":{"attr1":"xxx","attr2",...}}} |
| /open/res/query/option | 查询设备的某些资源当前值 | {"openId":"xxx","**did**":"xxx","**option**":["attr1","attr2",...]} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0(errorcode), "result":{"did":"xxx","data":{"attr1":"xxx","attr2",...}}} |