---
title: "编译器错误 CS0439 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0430"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0439"
ms.assetid: 5cbac869-1b1b-45f9-98c8-38c17348035f
caps.latest.revision: 10
caps.handback.revision: 10
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0439
外部别名声明必须位于命名空间中定义的所有其他元素之前  
  
 当 `extern` 声明出现在同一命名空间中的其他项（如 `using` 声明）后时，将发生此错误。`extern` 声明必须出现在所有其他命名空间元素之前。  
  
## 示例  
 下面的示例生成 CS0439：  
  
```  
// CS0439.cs using System; extern alias MyType;   // CS0439 // To resolve the error, make the extern alias the first line in the file. public class Test { public static void Main() { } }  
```