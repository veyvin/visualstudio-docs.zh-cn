---
title: "不允许通过用单个类型说明符声明多个变量来进行显式初始化 | Microsoft Docs"
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
  - "bc30671"
  - "vbc30671"
helpviewer_keywords: 
  - "BC30671"
ms.assetid: 57bbdd58-b58d-4144-8fa6-366a7167df27
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 不允许通过用单个类型说明符声明多个变量来进行显式初始化
当在同一行声明多个变量时，不允许进行初始化。  
  
 **错误 ID：**BC30671  
  
### 更正此错误  
  
1.  分别声明并初始化每个项。  
  
2.  一起声明多个项，然后初始化每个项；例如：  
  
    ```  
    Dim x, b, i As Integer x = 9 : b = 9 : i = 9 ' ":" is the same as a new line.  
    ```  
  
## 请参阅  
 [Dim 语句](/dotnet/visual-basic/language-reference/statements/dim-statement)   
 [变量声明](/dotnet/visual-basic/programming-guide/language-features/variables/variable-declaration)