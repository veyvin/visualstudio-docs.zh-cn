---
title: "“&lt;specifier&gt;”在 WithEvents 声明中无效。 | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30234"
  - "bc30234"
helpviewer_keywords: 
  - "BC30234"
ms.assetid: f7c9e2e4-d2f6-4bcf-bea9-a290c4c64804
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;specifier&gt;”在 WithEvents 声明中无效。
`Dim` 语句包含一个关键字（如 `ReadOnly`），此关键字与 `WithEvents` 关键字结合使用时无效。  
  
 **错误 ID：**BC30234  
  
### 更正此错误  
  
1.  从 `Dim` 语句中删除无效的关键字。  
  
## 请参阅  
 [Dim 语句](/dotnet/visual-basic/language-reference/statements/dim-statement)   
 [WithEvents](/dotnet/visual-basic/language-reference/modifiers/withevents)