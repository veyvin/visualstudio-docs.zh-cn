---
title: "编译器错误 CS0192 | Microsoft Docs"
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
  - "CS0192"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0192"
ms.assetid: d3fb6d18-dbf3-42c3-a280-afe55b97c2d1
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0192
无法向静态只读字段“name”的字段传递 ref 或 out（在静态构造函数中除外）  
  
 除在构造函数中以外，无法将具有 [readonly](/dotnet/csharp/language-reference/keywords/readonly) 关键字标记的字段（变量）传递到 [ref](/dotnet/csharp/language-reference/keywords/ref) 或 [out](/dotnet/csharp/language-reference/keywords/out) 参数。 有关更多信息，请参见[字段](/dotnet/csharp/programming-guide/classes-and-structs/fields)。  
  
 如果 `readonly` 字段为 [static](/dotnet/csharp/language-reference/keywords/static) 且构造函数未标记为 `static`，也会导致 CS0192。  
  
## 示例  
 以下示例生成 CS0192。  
  
```  
// CS0192.cs class MyClass { public readonly int TestInt = 6; static void TestMethod(ref int testInt) { testInt = 0; } MyClass() { TestMethod(ref TestInt);   // OK } public void PassReadOnlyRef() { TestMethod(ref TestInt);   // CS0192 } public static void Main() { } }  
```