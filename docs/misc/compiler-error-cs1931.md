---
title: "编译器错误 CS1931 | Microsoft Docs"
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
  - "CS1931"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1931"
ms.assetid: c0071c3d-ae11-4073-87df-508150daef68
caps.latest.revision: 6
caps.handback.revision: 6
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1931
范围变量“variable”与“variable”以前的声明存在冲突。  
  
 正如其他各个声明一样，范围变量的声明必须具有在变量声明空间中唯一的标识符。  
  
### 更正此错误  
  
1.  为范围变量提供唯一名称。  
  
## 示例  
 下面的代码生成 CS1931，因为该标识符 `x` 既用作 `Main` 中的本地变量，也用作查询表达式中的范围变量：  
  
```  
// cs1931.cs class Test { static void Main() { int x = 1; var y = from x in Enumerable.Range(1, 100) // CS1931 select x; } }  
```  
  
## 请参阅  
 [LINQ 查询表达式](/dotnet/csharp/programming-guide/linq-query-expressions/index)