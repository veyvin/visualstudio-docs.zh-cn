---
title: "方法不能同时包含“Try”语句和“On Error”或“Resume”语句 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30544"
  - "bc30544"
helpviewer_keywords: 
  - "BC30544"
ms.assetid: 1e75d5fe-9a6b-43c2-9749-1f2d7ce5b10d
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 方法不能同时包含“Try”语句和“On Error”或“Resume”语句
你已将 `Try` 语句和 `On Error` 或 `Resume` 合并。  
  
 **错误 ID：**BC30544  
  
### 更正此错误  
  
1.  删除 `On Error` 或 `Resume`。  
  
## 请参阅  
 [Visual Basic 的结构化异常处理概述](http://msdn.microsoft.com/zh-cn/bb81af80-a735-4873-9711-6151a48e418a)   
 [Try...Catch...Finally 语句](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)