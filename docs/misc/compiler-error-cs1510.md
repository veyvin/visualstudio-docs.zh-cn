---
title: "编译器错误 CS1510 | Microsoft Docs"
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
  - "CS1510"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1510"
ms.assetid: 3f5a69f1-7672-4194-a4ee-5753370fc736
caps.latest.revision: 10
caps.handback.revision: 10
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1510
ref 或 out 参数必须是可赋值的变量  
  
 在方法调用中只有一个变量可以作为 [ref](/dotnet/csharp/language-reference/keywords/ref) 参数传递。`ref` 值与传递指针类似。  
  
## 示例  
 下面的示例生成 CS1510：  
  
```  
// CS1510.cs public class C { public static int j = 0; public static void M(ref int j) { j++; } public static void Main () { M (ref 2);   // CS1510, can't pass a number as a ref parameter // try the following to resolve the error // M (ref j); } }  
```