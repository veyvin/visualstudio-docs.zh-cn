---
title: "Option Strict On 不允许从“&lt;type1&gt;”到“&lt;type2&gt;”的隐式转换 | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30512"
  - "vbc30512"
helpviewer_keywords: 
  - "BC30512"
ms.assetid: b9756d48-05fa-4027-8a80-b4a0ef92099d
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Option Strict On 不允许从“&lt;type1&gt;”到“&lt;type2&gt;”的隐式转换
你已尝试将一种类型转换为另一种可能无法包含值的类型，例如，将 `Long` 转换为 `Integer`，其中类型检查开关 \([Option Strict 语句](/dotnet/visual-basic/language-reference/statements/option-strict-statement)\) 已被设置为 `On`。  
  
 此转换类型称为*收缩转换*，它在运行时可能会失败。 正因如此，`Option Strict On` 不允许隐式收缩转换。  
  
 **错误 ID：**BC30512  
  
### 更正此错误  
  
1.  确定是否存在从 `<type1>` 到 `<type2>` 的任何类型的转换。 如果二者都为 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 基本类型，或如果二者都为类的实例，则通常可以通过参考 [扩大转换和收缩转换](/dotnet/visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions) 中的表做出此判断。  
  
2.  如果只存在从 `<type1>` 到 `<type2>` 的收缩转换，则应使用显式强制转换。 如果转换失败，[CType 函数](/dotnet/visual-basic/language-reference/functions/ctype-function) 和 [DirectCast 运算符](/dotnet/visual-basic/language-reference/operators/directcast-operator) 关键字会引发运行时异常。 如果转换失败，[TryCast 运算符](/dotnet/visual-basic/language-reference/operators/trycast-operator) 关键字仅适用于引用类型并返回 [Nothing](/dotnet/visual-basic/language-reference/nothing)。  
  
3.  如果存在收缩转换并且程序可以容忍运行时失败，或者你确信不可能发生运行时失败，则可以在源代码的开头指定 `Option Strict Off`。 但你仍应将转换括在 [Try...Catch...Finally 语句](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement) 块内以避免意外结果或程序提前终止。  
  
4.  如果不存在从 `<type1>` 到 `<type2>` 的转换，则必须重新计算程序逻辑。 你可能需要编写代码，该代码可以向对应于 `<type1>` 的预期值的 `<type2>` 分配值。  
  
5.  如果不存在从 `<type1>` 到 `<type2>` 的转换，并且其中一种类型是你已定义的类或结构，则你可能需要定义该类型与另一种类型之间的来回转换运算符。 有关更多信息，请参见[如何：定义转换运算符](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)。  
  
6.  在所有情况下并且一般原则是，除非可以捕获 `Catch` 块中的故障并有效地处理它们，否则应避免使用收缩转换。  
  
## 请参阅  
 [Option Strict 语句](/dotnet/visual-basic/language-reference/statements/option-strict-statement)   
 [扩大转换和收缩转换](/dotnet/visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions)   
 [CType 函数](/dotnet/visual-basic/language-reference/functions/ctype-function)   
 [DirectCast 运算符](/dotnet/visual-basic/language-reference/operators/directcast-operator)   
 [TryCast 运算符](/dotnet/visual-basic/language-reference/operators/trycast-operator)   
 [Nothing](/dotnet/visual-basic/language-reference/nothing)   
 [Try...Catch...Finally 语句](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)   
 [如何：定义转换运算符](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)