---
title: "在“Select”、“Case”语句的表达式中使用了 Object 类型的操作数；可能会发生运行时错误 | Microsoft Docs"
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
  - "vbc42036"
  - "bc42036"
helpviewer_keywords: 
  - "BC42036"
ms.assetid: f11e9c9f-aa66-4eb1-8f49-abf713bef885
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 在“Select”、“Case”语句的表达式中使用了 Object 类型的操作数；可能会发生运行时错误
`Select`...`Case` 构造使用一个或多个 [Object 数据类型](/dotnet/visual-basic/language-reference/data-types/object-data-type) 表达式。  
  
 当变量或表达式的计算结果为 `Object` 时，编译器必须执行*后期绑定*，这将导致在运行时产生额外的操作。 它还使应用程序易于发生潜在的运行时错误。 例如，如果将 <xref:System.Windows.Forms.Form> 分配到 `Object` 变量，然后尝试将它与数字进行比较，则运行时会引发 <xref:System.InvalidCastException>，因为 Visual Basic 不能将 <xref:System.Windows.Forms.Form> 对象转换为数字值。  
  
 `Select`...`Case` 构造中的表达式均应属于相同的数据类型或者属于能够彼此相互转换的密切相关的数据类型。 这是因为每个 `Case` 语句将针对 `Select`...`Case` 构造基于的测试表达式至少比较一个值。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的信息，请参见 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC42036  
  
### 更正此错误  
  
-   如果可能，排列所有表达式，使计算结果为与定义比较运算符相关的数据类型。  
  
## 请参阅  
 [Select...Case 语句](/dotnet/visual-basic/language-reference/statements/select-case-statement)   
 [算术运算符 \(Visual Basic\)](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators)   
 [比较运算符 \(Visual Basic\)](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators)