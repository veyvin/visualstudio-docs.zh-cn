---
title: "“Continue Do”只能出现在“Do”语句内 | Microsoft Docs"
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
  - "vbc30782"
  - "bc30782"
helpviewer_keywords: 
  - "BC30782"
ms.assetid: c6b35e63-4d84-449d-9685-41a1bc0a7f35
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “Continue Do”只能出现在“Do”语句内
`Continue Do` 语句只能出现在 `Do...Loop` 循环内。  
  
 **错误 ID:** BC30782  
  
### 更正此错误  
  
1.  如果 `Continue Do` 语句在 `For...Next` 循环中，请将该语句更改为 `Continue For`。  
  
2.  如果 `Continue Do` 语句在 `While...End While` 循环中，请将该语句更改为 `Continue While`。  
  
3.  否则，请删除 `Continue Do` 语句。  
  
## 请参阅  
 [Continue 语句](/dotnet/visual-basic/language-reference/statements/continue-statement)   
 [Do...Loop 语句](/dotnet/visual-basic/language-reference/statements/do-loop-statement)