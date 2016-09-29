# 设备属性获取

AIOT开放API可供第三方应用查询设备属性。

| API | 描述 | payload | header | response |
| -- | -- | -- | -- | -- |
| /open/resource/query | 查询设备有哪些资源 | {"openId":"xxx","**did**":"xxx"} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0|errorcode, "result":{"did":"xxx","attr":[{"attr1":"xxx","name":"xxx","minValue":"xxx","maxValue":"xxx","enum":[xx,xx,xx]}]}} |
| /open/res/query/option | 查询设备的某些资源当前值 | {"openId":"xxx","**did**":"xxx","**option**":["attr1","attr2",...]} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0(errorcode), "result":{"did":"xxx","data":{"attr1":"xxx","attr2",...}}} |
| /open/res/query/history/option | 查询资源历史 | {"openId":"xxx","did":"xxx","startDate":"2016-02-10", "endDate":"2016-03-10", "option":["attr1", "attr2",…],"startCount":xx,"endCount":xx} | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} | {"code":0(errorcode), "result":{"did":"11111","data":[{"attr1":"value","time":xxxxx},{"attr1":"value","time":xxxx},{"attr2":"value","time":xxxxx},{},...]}} |

> - openId: 用户id
> - did: 设备id
> - attr: 设备的资源（详见资源定义文档）
> - startDate: 资源历史的开始日期
> - endDate: 资源历史的结束日期
> - startCount: 查询结果分页的启始数目
> - endCount: 查询结果分页的截止数目