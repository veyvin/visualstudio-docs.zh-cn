---
title: "“New”不能在类“&lt;classname&gt;”上使用，因为它包含尚未被重写的“MustOverride”成员 | Microsoft Docs"
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
  - "bc30376"
  - "vbc30376"
helpviewer_keywords: 
  - "BC30376"
ms.assetid: f3aed05a-8202-4d2d-9c49-3c000d055116
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “New”不能在类“&lt;classname&gt;”上使用，因为它包含尚未被重写的“MustOverride”成员
已在包含未被重写的 `MustOverride` 成员的类上尝试使用 `New`。  
  
 **错误 ID：**BC30376  
  
### 更正此错误  
  
-   删除 `New` 语句。  
  
## 请参阅  
 [MustOverride](/dotnet/visual-basic/language-reference/modifiers/mustoverride)