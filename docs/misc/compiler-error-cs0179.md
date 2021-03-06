---
title: "编译器错误 CS0179 | Microsoft Docs"
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
  - "CS0179"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0179"
ms.assetid: bef000ca-64d7-4809-b2a0-de6927b04b0d
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0179
“member”不能是外部的，也无法声明主体  
  
 当类成员标记为[外部](/dotnet/csharp/language-reference/keywords/extern)，这意味着该成员的定义位于另一个文件中。 因此，标记为 **外部**的类成员不能在类中定义。 删除 `extern` 关键字或删除该定义。 有关详细信息，请参阅[方法](/dotnet/csharp/programming-guide/classes-and-structs/methods)。  
  
 以下示例生成 CS0179：  
  
```  
// CS0179.cs public class MyClass { public extern int ExternMethod(int aa)   // CS0179 { return 0; } // try the following line instead // public extern int ExternMethod(int aa); public static void Main() { } }  
```