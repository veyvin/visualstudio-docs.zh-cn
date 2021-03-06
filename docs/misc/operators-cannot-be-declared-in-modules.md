---
title: "运算符不能在模块中声明 | Microsoft Docs"
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
  - "bc33018"
  - "vbc33018"
helpviewer_keywords: 
  - "BC33018"
ms.assetid: 10a8fd2d-2af7-4f90-9f2a-50c07ebf7589
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 运算符不能在模块中声明
[Operator 语句](/dotnet/visual-basic/language-reference/statements/operator-statement) 出现在模块定义中。  
  
 可以将运算符定义为正在定义的类或结构的一部分。 运算符至少必须将该类或结构作为其操作数之一。  
  
 运算符必须将编程元素的实例用作操作数之一，只有类和结构才有实例。 因此，你不能将运算符定义为其他任何编程元素的一部分。  
  
 **错误 ID：**BC33018  
  
### 更正此错误  
  
-   如果需要对该模块进行操作，请使用 [Function 语句](/dotnet/visual-basic/language-reference/statements/function-statement) 定义执行该操作的 `Function` 过程。  
  
-   此外，可以在模块中定义类或结构，然后在该类或结构上定义运算符。 但是，该运算符至少必须将该类或结构的实例作为其操作数之一。  
  
## 请参阅  
 [运算符过程](/dotnet/visual-basic/programming-guide/language-features/procedures/operator-procedures)   
 [如何：定义运算符](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [如何：定义转换运算符](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)