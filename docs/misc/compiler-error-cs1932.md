---
title: "编译器错误 CS1932 | Microsoft Docs"
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
  - "CS1932"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1932"
ms.assetid: fc927899-2d35-4d47-9ae9-8fc99295bb66
caps.latest.revision: 6
caps.handback.revision: 6
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1932
无法将“expression”赋值给范围变量  
  
 编译器必须能够推断出的某个范围变量的类型，不管其是在 `from` 子句中引入还是在 `let` 子句中引入。 其不能为 null，因为 null 不是一种类型，而且不能使用不安全类型的表达式对其赋值。  
  
### 更正此错误  
  
-   删除无效的赋值。  
  
-   将此表达式显式转换为允许的类型  
  
## 示例  
 下面的代码会生成 CS1932，因为不能推断范围变量的类型。 将值转换为预期类型以修复此错误，如下面的示例所示。  
  
```  
// CS1932.cs using System.Linq; class Test { static void Main() { var x = from i in Enumerable.Range(1, 100) let k = null // CS1932 // Try the following line instead. let k = (string) null select i; } }  
```  
  
## 请参阅  
 [LINQ 查询表达式](/dotnet/csharp/programming-guide/linq-query-expressions/index)