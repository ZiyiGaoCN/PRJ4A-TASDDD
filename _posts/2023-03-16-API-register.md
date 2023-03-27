---
layout: post
title: API——/register
categories: ['/register']
description: /register的API
keywords: keyword1, keyword2
mathjax: true
---
# URL `/register`
该API仅接受POST方法请求，方法请求均应当设置状态码为 405 Method Not Allowed，错误响应格式为：
```json
{
  "code": -3,
  "info": "Bad method"
}
```

## POST

请求增加一个账号。

- [ ] 加密功能
- [ ] 检查功能

### 请求体

```json
{
  "userName": "Alice",
  "password": "fsafojofjoajfodsajfjoijfsaoif.....",
  "userType": "labeler",
  "invitation_code": "asfjgwiqua"
}   
```

其中`userName`需要满足是长度在`3`到`20`之间。

`password`不能为明文传输，约定为XX加密方式。

`userType` 必须是 `LB`,`DM`,`IT`

`invitation_code`可以为空，长度限制为`10`。

### 成功响应体

状态码设置成`200`

```json
{
  "info": "Succeed",
  "code": 0
}
```

### 失败响应体

状态码为`500`,code码为`-1`

```json
{
    "code": "*",
    "info": "[Some message]"
}
```

`info`包括但不限于: `UserName existed`。
