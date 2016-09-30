# 开放接口调用规范


AIOT开放接口均使用HTTPS协议，需要在header中添加校验信息，在body中添加payload信息，返回结果为JSON格式。

- 开放接口统一域名: https://aiot-rpc.aqara.cn
- header部分的校验信息: ```{"Appid":"xxx","Appkey":"xxx","Access-Token":"xxx","Openid":"xxx"}```
- payload数据格式：JSON
- 返回结果数据格式：JSON

##例子

给出一个请求获取设备信息的API接口调用示范，如下：

- 获取设备信息API：/open/query/device
- https请求的URL：https://aiot-rpc.aqara.cn/open/query/device
- header：```{"Appid":"xxx","Appkey":"xxx","Access-Token":"xxx","Openid":"xxx"}```
- payload: ```{"openId":"xxx","did":"xxx"}```
- response: ```{"code":0(errorcode), "result":{"did":"xxx", "model":"xxx", "name":"xxx", "firmwareVersion": "xxx", "state":"xxx", "chipVersion":"xxx", "longitude":"xxx", "latitude":"xxx", ...}```

其中：

- Appid为第三方应用appId
- Appkey为第三方应用appKey
- Access-Token为用户Token（详见账户对接文档）
- Openid为用户在AIOT中的账号（详见账户对接文档）
- 

