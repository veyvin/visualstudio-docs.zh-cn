---
title: "“Exit Sub”在函数或属性中无效 | Microsoft Docs"
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
  - "bc30065"
  - "vbc30065"
helpviewer_keywords: 
  - "BC30065"
ms.assetid: d6426861-ba64-4dca-9100-262c6c058bd9
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “Exit Sub”在函数或属性中无效
`Exit Sub` 出现在 `Function` 过程或 `Property` 过程中。`Exit` 语句必须与它所在的块匹配。  
  
 **错误 ID：**BC30065  
  
### 更正此错误  
  
-   根据需要，用 `Exit Function` 或 `Exit Property` 语句替换 `Exit Sub`。  
  
## 请参阅  
 [Sub 过程](/dotnet/visual-basic/programming-guide/language-features/procedures/sub-procedures)   
 [Function 过程](/dotnet/visual-basic/programming-guide/language-features/procedures/function-procedures)   
 [Property 过程](/dotnet/visual-basic/programming-guide/language-features/procedures/property-procedures)