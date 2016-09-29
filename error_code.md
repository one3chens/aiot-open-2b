# 错误码

AIOT开放API的返回结果中，包含一个code字段，它的值是错误码，下面是定义出来的错误码：

| 类别 | code | 表示 | 说明 |
| -- | -- | -- | -- |
| SUCCESS | 0 | SUCCESS | 成功 |
| ERROR_PACKAGE | 100 | ERROR_TIMEOUT | Timeout, 超时 |
| ERROR_PACKAGE | 101 | ERROR_PACKAGE_ILLEGAL | 数据包非法 |
| ERROR_PACKAGE | 102 | ERROR_PACKAGE_DAMAGE | 数据包损坏 |
| ERROR_REQUEST | 301 | ERROR_REQUEST_PATH | 请求路径错误 |
| ERROR_REQUEST | 302 | ERROR_REQUEST_PARAMS | 请求参数错误 |
| ERROR_USER | 401 | ERROR_USER_NO_REG | 用户未注册 |
| ERROR_USER | 402 | ERROR_USER_NO_LOGIN | 用户未登录 |
| ERROR_USER | 403 | ERROR_USER_PERMISSION_DENIED | 拒绝用户访问，没有权限 |
| ERROR_USER | 411 | ERROR_PASSWORD_NOT_CORRECT | 密码错误 |
| ERROR_USER | 412 | ERROR_TOKEN_FAILED | Token失效 |
| ERROR_SERVER | 500 | ERROR_INTERNAL_SERVER | Server Error 服务器出错，服务器处理中出错 |