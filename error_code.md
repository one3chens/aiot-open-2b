# 错误码

AIOT开放API的返回结果中，包含一个code字段，它的值是错误码，下面是定义出来的错误码：

| 类别 | code | 表示 | 说明 |
| -- | -- | -- | -- |
| SUCCESS | 0 | SUCCESS | 成功 |
| ERROR_PACKAGE | 100 | ERROR_TIMEOUT | Timeout, 超时 |
| ERROR_PACKAGE | 101 | ERROR_PACKAGE_ILLEGAL | 数据包非法 |
| ERROR_PACKAGE | 102 | ERROR_PACKAGE_DAMAGE | 数据包损坏 |
| ERROR_REQUEST | 301 | ERROR_REQUEST_PATH | 请求路径错误 |
| ERROR_REQUEST | 302 | ERROR_REQUEST_PARAMS |请求参数错误 |
