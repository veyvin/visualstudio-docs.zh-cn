---
title: "编译器错误 CS0236 | Microsoft Docs"
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
  - "CS0236"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0236"
ms.assetid: 1522c421-744f-441f-9e05-6bb31311ab2a
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0236
字段初始值设定项无法引用非静态字段、方法或属性“field”  
  
 实例字段不能用于初始化方法之外的其他实例字段。 如果正在尝试初始化方法之外的变量，请考虑在类构造函数内执行此初始化。 有关更多信息，请参见[方法](/dotnet/csharp/programming-guide/classes-and-structs/methods)。  
  
 以下示例生成 CS0236：  
  
```  
// CS0236.cs public class MyClass { public int i = 5; public int j = i;  // CS0236 public int k;      // initialize in constructor MyClass() { k = i; } public static void Main() { } }  
```