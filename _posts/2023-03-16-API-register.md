---
layout: post
title: API——/register
categories: ['/register']
description: /register的API
keywords: keyword1, keyword2
mathjax: true
---
# URL `/register`

## PUT

请求增加一个账号。

### 请求体

```json
{
  "uesrName": "Alice",
  "password": "fsafojofjoajfodsajfjoijfsaoif.....",
  "role": "player",
  "inviteNumber": ""
}   
```

其中`UserName`需要满足是长度在`3`到`20`之间。

`password`不能为明文传输，约定为XX加密方式。

`role` 必须是 `player`,`distributor`,`intermediary`

`inviteNumber`可以为空，长度限制为`10`。

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
