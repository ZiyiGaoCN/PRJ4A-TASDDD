---
layout: post
title: Task DB
categories: [cate1, cate2]
description: some word here
keywords: keyword1, keyword2
---

### Task DB

该数据库中包含了

`id`:注册时生成，为主键，不可修改

`demander`:需求方

`task_type`:任务类型
- TC (text classification): 文字分类
- IC (Image classification): 图片分类

`task_name`:任务名称（需求方自己使用，用户不可见），长度不超过50个字符（25个汉字）

`title`:标题（给标注方看的），长度不超过50个字符（25个汉字）

`summary`:简介，长度不超过300个字符（约150个汉字）

`time_limit`:限时，以小时为单位

`reward`:完成并通过审核后给标注方奖励的信用分/金额

`created_time`:任务创建时间

`is_active`:是否仍有效（可标注）

### Assignment DB

标注任务中的某个标注项（类似问卷中的一道题），是所有标注项的父类（抽象类）

该数据库中包含了

`instruction`:解释标注原则等，知道标注方进行标注

`task`:所属标注任务

`id`:在任务中是第几个标注项，从1开始

### Text Classification Assignment DB

给定一段文字，选出正确选项（单选）

例如：情感分类

该数据库中包含了

`text`:待分类的文本，不超过1000个字符（500个汉字）

### Image Classification Assignment DB

给定一张图片，选出正确选项（单选）

例如：动物分类

该数据库中包含了

`image_url`:待分类的图片的url，不超过1000个字符

### Text Classification Choice DB

该数据库中包含了

`assignment`:所属的标注项

`description`:选项描述

`id`:在选项列表中的标号
