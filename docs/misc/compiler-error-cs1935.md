---
title: "编译器错误 CS1935 | Microsoft Docs"
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
  - "CS1935"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1935"
ms.assetid: d5dda801-fbf3-4340-bfe1-f9409f2d344d
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1935
未能找到源类型“type”的查询模式的实现。 找不到“method”。 是否缺少对“System.Core.dll”的引用，或者缺少针对“System.Linq”的 using 指令？  
  
 在查询中的源类型必须是 `IEnumerable`、`IEnumerable<T>` 或派生的类型，或者你或其他人已为其实现了标准查询运算符的类型。 如果源类型为 `IEnumerable` 或 `IEnumerable<T>`，必须添加一个对 system.core.dll 的引用和一个用于 System.Linq 命名空间的 `using` 指令，以便将标准查询运算符扩展方法引入作用域。 必须以同样方式，使用 `using` 指令，以及（如有必要）使用对程序集的引用将标准查询运算符的自定义实现引入作用域。  
  
### 更正此错误  
  
1.  添加所需的 using 指令和对项目的引用。  
  
## 示例  
 以下代码生成 CS1935，因为用于 System.Linq 的 `using` 指令被注释掉：  
  
```  
// cs1935.cs // CS1935 using System; using System.Collections.Generic; // using System.Linq; class Test { static int Main() { int[] nums = {0,1,2,3,4,5}; IEnumerable<int> e = from n in nums where n > 3 select n; return 0; } }  
```  
  
## 请参阅  
 [Standard Query Operators Overview](../Topic/Standard%20Query%20Operators%20Overview.md)