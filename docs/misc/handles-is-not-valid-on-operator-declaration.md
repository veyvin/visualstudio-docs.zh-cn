---
title: "“Handles”在运算符声明上无效 | Microsoft Docs"
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
  - "bc33003"
  - "vbc33003"
helpviewer_keywords: 
  - "BC33003"
ms.assetid: 8336402c-9393-4e8e-834d-55c2268f24f6
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “Handles”在运算符声明上无效
[Operator 语句](/dotnet/visual-basic/language-reference/statements/operator-statement) 指定 [Handles](/dotnet/visual-basic/language-reference/statements/handles-clause) 关键字。  
  
 只有 `Sub` 过程可处理事件。`Operator` 过程不能处理。 有关事件处理程序的详细信息，请参阅[如何：在 Visual Basic 中调用事件处理程序](../Topic/How%20to:%20Call%20an%20Event%20Handler%20in%20Visual%20Basic.md)。  
  
 `Operator` 过程需要 `Public` 和 `Shared` 两个关键字，而转换运算符需要 `Widening` 或 `Narrowing` 关键字。 有关更多信息，请参见[运算符过程](/dotnet/visual-basic/programming-guide/language-features/procedures/operator-procedures)。  
  
 **错误 ID：**BC33003  
  
### 更正此错误  
  
-   如果你想要此过程处理事件，请将其重写为 `Sub` 过程。  
  
-   如果你想要此过程定义运算符，请从其声明中删除 `Handles` 关键字。  
  
## 请参阅  
 [Operator 语句](/dotnet/visual-basic/language-reference/statements/operator-statement)   
 [如何：定义运算符](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [如何：定义转换运算符](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)