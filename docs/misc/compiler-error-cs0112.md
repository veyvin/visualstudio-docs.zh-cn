---
title: "编译器错误 CS0112 | Microsoft Docs"
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
  - "CS0112"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0112"
ms.assetid: 6741c7c4-8553-4bbe-b950-4f908e8d9ba3
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0112
静态成员“函数”不能标记为 override、virtual 或 abstract  
  
 使用 `override`、**virtual** 或 **abstract** 关键字的任何方法声明也不能使用 **static** 关键字。  
  
 有关详细信息，请参阅[方法](/dotnet/csharp/programming-guide/classes-and-structs/methods)。  
  
 下面的示例生成 CS0112:  
  
```  
// CS0112.cs namespace MyNamespace { abstract public class MyClass { public abstract void Foo(); } public class MyClass2 : MyClass { override public static void Foo()   // CS0112, remove static keyword { } public static int Main() { return 0; } } }  
```