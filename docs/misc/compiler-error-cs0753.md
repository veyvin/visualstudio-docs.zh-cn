---
title: "编译器错误 CS0753 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0753"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0753"
ms.assetid: 287dd9da-da74-4290-9fa1-21ef1a8150fe
caps.latest.revision: 5
caps.handback.revision: 5
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0753
只有方法、类、结构或接口可以是分部形式。  
  
 [partial](/dotnet/csharp/language-reference/keywords/partial-type) 修饰符只能用于类、结构、接口和方法。  
  
### 更正此错误  
  
1.  从变量或语言构造中删除 `partial` 修饰符。  
  
## 示例  
 下面的代码生成 CS0753：  
  
```  
// cs0753.cs using System; public partial class C { partial int num; // CS0753 public static int Main() { return 1; } }  
```  
  
## 请参阅  
 [分部类和方法](/dotnet/csharp/programming-guide/classes-and-structs/partial-classes-and-methods)