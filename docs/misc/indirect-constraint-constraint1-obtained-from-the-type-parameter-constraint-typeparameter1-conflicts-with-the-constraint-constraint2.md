---
title: "从类型形参约束“&lt;typeparameter1&gt;”获取的间接约束“&lt;constraint1&gt;”与约束“&lt;constraint2&gt;”冲突 | Microsoft Docs"
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
  - "bc32111"
  - "vbc32111"
helpviewer_keywords: 
  - "BC32111"
ms.assetid: b03b5840-5318-4844-b2da-1bca4c28d097
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 从类型形参约束“&lt;typeparameter1&gt;”获取的间接约束“&lt;constraint1&gt;”与约束“&lt;constraint2&gt;”冲突
使用因直接和间接约束的组合而导致冲突的约束声明了一个泛型类型。  
  
 以下语句可能会生成此错误。  
  
 `Public Class testClass(Of t1 As {t2, Class}, t2 As Structure)`  
  
 间接约束 `Structure` 和直接约束 `Class` 会导致类型形参 `t1` 冲突，原因是 `Structure` 约束要求相应的类型实参为值类型，而 `Class` 要求其为引用类型。  
  
 **错误 ID：**BC32111  
  
### 更正此错误  
  
-   更改类型形参约束以避免约束冲突。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [类型列表](/dotnet/visual-basic/language-reference/statements/type-list)   
 [结构 \(Visual Basic\)](http://msdn.microsoft.com/zh-cn/263ce115-ac36-4c05-8cb7-0e0eead5c6d0)   
 [类 \(Visual Basic\)](http://msdn.microsoft.com/zh-cn/0777c6e6-46bc-451b-ad70-57b49d4ef4f7)   
 [值类型和引用类型](/dotnet/visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types)