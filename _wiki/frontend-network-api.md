---
layout: wiki
title: 使用API接口
cate1: 前端
cate2: 网络请求
description: Axios 环境
keywords: Axios
---

## 使用API进行网络请求

### 1. 通用的API接口

```typescript
import {request} from '/utils/network';

request(url: string,
    method: "GET" | "POST" | "PUT" | "DELETE",
    data?: any);
```

#### Workflow

- [ ] 目前的处理还比较粗糙，需要更新。

1. 传入`url`，`method`，`data`。
2. 首先，调用axios的`request`方法，传入`url`，`method`，`data`，与后端进行通讯。
3. 得到后端的响应`response`，如果后端在此此期间出现错误，那么会抛出`UNKNOWN_ERROR`错误。
4. 如果后端返回的`response`的`code`为`0`，那么返回`response`的`data`。
5. 如果后端返回的`response`的`code`不为`0`，其中`UNKNOWN_ERROR`错误。

Note: `UNKNOWN_ERROR`错误是前端定义的错误，其类型为`NetworkError`，定义在`/utils/network.ts`中。

### 2. 非通用API
