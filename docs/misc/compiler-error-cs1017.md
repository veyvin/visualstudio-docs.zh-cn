---
title: "编译器错误 CS1017 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1017"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1017"
ms.assetid: e0902e8a-b042-4711-a8a6-83456a3f88cb
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1017
catch 子句不能跟在 try 语句的常规 catch 子句之后  
  
 不接受任何参数的 `catch` 块必须是一系列 `catch` 块中的最后一个。 有关异常的详细信息，请参阅[异常处理语句](/dotnet/csharp/language-reference/keywords/exception-handling-statements)。  
  
## 示例  
 下面的示例生成 CS1017：  
  
```  
// CS1017.cs using System; namespace x { public class b : Exception { } public class a { public static void Main() { try { } catch   // CS1017, must be last catch { } catch(b) { throw; } } } }  
```