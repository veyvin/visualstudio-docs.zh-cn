---
title: "“End Select”前面必须是匹配的“Select Case” | Microsoft Docs"
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
  - "bc30088"
  - "vbc30088"
helpviewer_keywords: 
  - "BC30088"
ms.assetid: 9de8c0d4-4ce9-45cf-98d6-8f68bba507a5
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “End Select”前面必须是匹配的“Select Case”
出现 `End Select` 语句，但没有相应的 `Select` 或 `Select Case` 语句。`End Select` 前面必须是 `Select` 或 `Select Case` 语句。  
  
 **错误 ID：**BC30088  
  
### 更正此错误  
  
1.  如果此 `Select` 块属于一组嵌套的 `Select` 块，请确保每个块均已正确终止。  
  
2.  验证 `Select` 块中的其他控制结构是否被正确终止。  
  
3.  检查此 `Select` 块的格式是否正确设置。  
  
## 请参阅  
 [Select...Case 语句](/dotnet/visual-basic/language-reference/statements/select-case-statement)