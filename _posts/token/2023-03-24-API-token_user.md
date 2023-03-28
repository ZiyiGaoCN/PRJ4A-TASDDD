---
layout: post
title: API————/token/user请求
categories: ['token','user']
description: 请求用户的基本数据信息
keywords: 
mathjax: true
---
# URL `token/user`
## POST
- [x] 已完成填写，责任人：高子翼

使用`token`，访问用户的基本数据信息。

后端需要首先检查是否存在该`token`,如果存在需要更新过期时间。

检查成功后，后端需要获得该`token`对应`user`，并且返回`user`的对应信息。

### 请求体
- [x] 请前端同学完成，责任人：高子翼

```json
{
    "token":"123213123"
}
```

### 成功响应体

- [√] 请后端同学完成，责任人：张珈铭

```json
{
  "info": "Succeed",
  "code": 0,
  "data": {
    "uid": 1,
    "username": "Alice",
    "userType": "LB",
    "accPoints": 0,
    "creditScore": 100,
    "membership": 0,
    "invitationCode": "abcdefg",
  }
}
```
### 失败响应体
- [√] 请后端同学完成，责任人：张珈铭

状态码为`500`,code码为`-1`
```json
{
    "code": -1,
    "info": "[Some message]"
}
```

`info`包括但不限于: `Token not existed` `Token has expired`.