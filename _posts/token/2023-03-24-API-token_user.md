---
layout: post
title: API——/login
categories: ['/token/user']
description: /token/user的API
keywords: keyword1, keyword2
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

- [ ] 请后端同学完成，责任人：

```json
{
  "info": "Succeed",
  "code": 0,
  "data": {
    
  }
}
```
### 失败响应体
- [ ] 请后端同学完成，责任人：

状态码为`None`,code码为`None`
```json
{
    "code": -1,
    "info": "[Some message]"
}
```

`info`包括但不限于: `Invalid username or password`.