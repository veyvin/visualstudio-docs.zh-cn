---
title: "构造函数无法实现接口方法。 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30550"
  - "vbc30550"
helpviewer_keywords: 
  - "BC30550"
ms.assetid: 982a767d-9174-408e-bdcf-ae0d96f88cef
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 构造函数无法实现接口方法。
你尝试使用 `New` 关键字实现接口方法，这是无效的。  
  
 **错误 ID：**BC30550  
  
### 更正此错误  
  
-   使用 `Implements` 关键字实现接口。  
  
## 请参阅  
 [Implements 语句](/dotnet/visual-basic/language-reference/statements/implements-statement)   
 [不在生成中：接口概述](http://msdn.microsoft.com/zh-cn/f96bb470-c1b8-4c73-89bc-6f536b798da1)