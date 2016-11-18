# 设备属性获取

AIOT开放API可供第三方应用查询设备属性。

| API | /open/res/query |
| --: | :-- |
| **描述** | 查询设备有哪些资源 |
| **header** | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} |
| **payload** | {"openId":"xxx","**did**":"xxx"} |
| **response** | {"code":0(errorcode), "result":{"did":"xxx","attr":[{"attr1":"xxx","name":"xxx","minValue":"xxx","maxValue":"xxx","enum":[xx,xx,xx]}]}} |

| API | /open/res/query/option |
| --: | :-- |
| **描述** | 查询设备的某些资源当前值 |
| **header** | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} |
| **payload** | {"openId":"xxx","**did**":"xxx","**option**":["attr1","attr2",...]} |
| **response** | {"code":0(errorcode), "result":{"did":"xxx","data":{"attr1":"xxx","attr2",...}}} |

| API | /open/res/query/option/extended |
| --: | :-- |
| **描述** | 查询设备的某些资源当前值(易扩展版) |
| **header** | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} |
| **payload** | {"openId":"xxx","**did**":"xxx","**option**":["attr1","attr2",...]} |
| **response** | {"code":0(errorcode), "result":[{"did":"xxx","attr":"xxx","value":"xxx","time":xxx},{"did":"xxx","attr":"xxx","value":"xxx","time":xxx},..]} |

| API | /open/res/query/user |
| --: | :-- |
| **描述** | 查询用户下所有设备的资源当前值 |
| **header** | {"**Appid**":"xxx","**Appkey**":"xxx","Openid":"xxx","**Access-Token**":"xxx"} |
| **payload** | {"openId":"xxx"} |
| **response** | {"code":0(errorcode), "result":[{"did":"xxx","attr":"xxx","value":"xxx","time":xxx},{"did":"xxx","attr":"xxx","value":"xxx","time":xxx},..]} |

> - openId: 用户id
> - did: 设备id
> - attr: 设备的资源（详见资源定义文档）
> - startDate: 资源历史的开始日期
> - endDate: 资源历史的结束日期
> - startCount: 查询结果分页的启始数目
> - endCount: 查询结果分页的截止数目
> - time: 时间戳（单位为秒）