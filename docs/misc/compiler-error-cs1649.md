---
title: "编译器错误 CS1649 | Microsoft Docs"
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
  - "CS1649"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1649"
ms.assetid: 6355c7f2-157c-441d-8925-500062988636
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1649
无法向只读字段“identifier”的成员传递 ref 或 out 参数（构造函数中除外）  
  
 如果将变量作为 `ref` 或 `out` 参数传递给一个属于`readonly` 字段成员的函数，则会发生此错误。 由于该函数可能修改 `ref` 和 `out` 参数，所以这是不允许的。 若要解决此错误，请删除字段上的 `readonly` 关键字，或者不要将 `readonly` 字段的成员传递给该函数。 例如，你可以尝试创建一个可修改的临时变量，并将该临时变量作为 `ref` 参数传递，如下面的示例所示。  
  
## 示例  
 下面的示例生成 CS1649：  
  
```  
// CS1649.cs public struct Inner { public int i; } class Outer { public readonly Inner inner = new Inner(); } class D { static void f(ref int iref) { } static void Main() { Outer outer = new Outer(); f(ref outer.inner.i);  // CS1649 // Try this code instead: // int tmp = outer.inner.i; // f(ref tmp); } }  
```