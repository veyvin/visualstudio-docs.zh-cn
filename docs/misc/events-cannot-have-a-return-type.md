---
title: "事件不能有返回类型 | Microsoft Docs"
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
  - "bc30032"
  - "vbc30032"
helpviewer_keywords: 
  - "BC30032"
ms.assetid: 4cd3bffc-b5b2-4000-bfb9-7d6968e6fc62
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 事件不能有返回类型
事件可以接受参数，但不能直接返回值。  
  
 **错误 ID：**BC30032  
  
### 更正此错误  
  
-   从 `Event` 语句中删除返回类型。  
  
## 请参阅  
 [Event 语句](/dotnet/visual-basic/language-reference/statements/event-statement)