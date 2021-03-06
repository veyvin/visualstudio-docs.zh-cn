---
title: "无法推断“&lt;typeparametername&gt;”类型形参 | Microsoft Docs"
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
  - "bc36572"
  - "vbc36572"
helpviewer_keywords: 
  - "BC36572"
ms.assetid: 02264070-b055-4ab0-8d2a-eac4d90d9fdf
caps.latest.revision: 4
caps.handback.revision: 4
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 无法推断“&lt;typeparametername&gt;”类型形参
在未提供类型实参列表的情况下调用泛型过程，某个类型实参的类型推理失败。  
  
 在调用泛型过程时，通常会为过程所定义的每个类型形参提供类型实参。 但是，还可以选择忽略整个类型实参列表。 执行此操作时，编译器将尝试推断调用上下文中每个类型实参的类型。 有关详细信息，请参见 [Visual Basic 中的泛型过程](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures) 中的“类型推理”。  
  
 **错误 ID:** BC36572  
  
### 更正此错误  
  
-   确保普通参数的类型是这样的：类型推理与为泛型过程声明的类型形参一致。  
  
     \- 或 \-  
  
-   调用具有完整类型实参列表的泛型过程，因此就不需要类型推理。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [类型列表](/dotnet/visual-basic/language-reference/statements/type-list)   
 [Visual Basic 中的泛型过程](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures)