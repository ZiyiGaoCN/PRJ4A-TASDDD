---
layout: wiki
title: ErrorType
cate1: 前端
cate2: 网络请求
description: Axios 环境
keywords: Axios
---

前端的错误类型定义为`NetworkError`，继承自`Error`,定义在`/utils/network.ts`中。

## NetworkError
内有
- `code`：错误码，`NetworkErrorType`类型,是一个`Enum`类型
- `message`：错误信息，`string`类型
  
## `code`NetworkErrorType
- `CORRUPTED_RESPONSE`：暂时还没有用到`0` 
- `UNKNOWN_ERROR`：未知错误 `1`

## `message`错误信息
格式为`[status code]message`。
- `status code`:后端返回的状态码
- `message`:为错误信息。