-----------
# 管理员专属
#### 功能

> 临时冻结用户

#### URL

> DELETE /api/v1/users/{id}?freezeTime=121212121&reason=冻结

#### 请求参数(queryString)

| 参数       | 必选  | 类型            | 默认值                                       | 说明     |
| :--------- | :---- | :-------------- | :------------------------------------------- | -------- |
| freezeTime | false | timestamp(毫秒) | currentTimeStamp + (1000 * 60 * 60 * 24 * 7) | 冻结时间 |
| reason     | true  | string          |                                              | 冻结原因 |

#### 响应：
##### 成功：204
##### 未登录: 401
##### 权限不足: 403
##### 用户不存在: 404
