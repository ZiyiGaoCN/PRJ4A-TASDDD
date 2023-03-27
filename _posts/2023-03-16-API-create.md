---
layout: post
title: API——/create
categories: ['/create']
description: /create的API
keywords: keyword1, keyword2
mathjax: true
---
# URL `/create`
该API仅接受POST方法请求，方法请求均应当设置状态码为 405 Method Not Allowed，错误响应格式为：
```json
{
  "code": -3,
  "info": "Bad method"
}
```
## POST

请求发布任务。

### 请求体
```json
{
  "demanderId": 1,
  "taskType": "TC",
  "taskName": "Text Classification",
  "title": "Text Sentiment Classification",
  "summary": "...",
  "timeLimit": 0.5,
  "reward": 1
}
```
`demanderId`:需求方的ID

`taskType`:任务类型（只能是以下两种之一）
- TC (text classification): 文字分类
- IC (Image classification): 图片分类

`taskName`:任务名称（需求方自己使用，用户不可见），长度不超过50个字符（25个汉字）

`title`:标题（给标注方看的），长度不超过50个字符（25个汉字）

`summary`:简介，长度不超过300个字符（约150个汉字）

`timeLimit`:限时，以小时为单位

`reward`:完成并通过审核后给标注方奖励的信用分/金额

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
    "code": -1,
    "info": "[Some message]"
}
```

`info`包括但不限于: `TaskName existed`.