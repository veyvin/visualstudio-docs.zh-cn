---
title: "“GoTo &lt;labelname&gt;”无效，因为“&lt;labelname&gt;”位于不包含此语句的“SyncLock”语句内 | Microsoft Docs"
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
  - "bc30755"
  - "vbc30755"
helpviewer_keywords: 
  - "BC30755"
ms.assetid: 95fb48c1-4982-45fc-81f0-f30cf0df173f
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “GoTo &lt;labelname&gt;”无效，因为“&lt;labelname&gt;”位于不包含此语句的“SyncLock”语句内
你不能分支到 `SyncLock` 块。  
  
 **错误 ID：**BC30755  
  
### 更正此错误  
  
-   重构你的代码，以便标签位于 `SyncLock` 块之前。  
  
## 请参阅  
 [SyncLock 语句](/dotnet/visual-basic/language-reference/statements/synclock-statement)