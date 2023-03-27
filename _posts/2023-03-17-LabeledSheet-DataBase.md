---
layout: post
title: LabeledSheet DB
categories: [cate1, cate2]
description: some word here
keywords: keyword1, keyword2
---

### Labeled Sheet DB

标注方完成标注后的"答卷"

该数据库中包含了

`labeler`:所属标注方

`task`:所属标注任务

`start_time`:开始标注时间

`finish_time`:结束标注时间

`status`:状态
- WE (waiting for examination): 等待审核
- AC (accepted): 审核通过
- RJ (rejected): 审核未通过

### Label DB

标注"答卷"中的某个具体标注项的标注

该数据库中包含了

`labeled_sheet`:所属"答卷"

### Text Classification Label DB

该数据库中包含了

`assignment`:所属标注项

`choice`:选中的选项

### Image Classification Label DB

该数据库中包含了

`assignment`:所属标注项

`choice`:选中的选项





