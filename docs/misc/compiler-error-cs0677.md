---
title: "编译器错误 CS0677 | Microsoft Docs"
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
  - "CS0677"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0677"
ms.assetid: 6a4a3703-9b44-4c4f-a564-8b437b1cb6b8
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0677
“变量”: 可变字段的类型不能是“类型”  
  
 使用 `volatile` 关键字声明的字段必须是以下类型之一：  
  
-   任何引用类型  
  
-   任何指针类型（在 `unsafe` 上下文中）  
  
-   `sbyte`, **byte**、**short**、`ushort`, `int`, `uint`, `char`, **float**、`bool` 类型  
  
-   基于任何上述类型的枚举类型  
  
 下面的示例生成 CS0677:  
  
```  
// CS0677.cs class TestClass { private volatile long i;   // CS0677 public static void Main() { } }  
```