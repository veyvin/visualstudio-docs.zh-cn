---
title: "编译器错误 CS1657 | Microsoft Docs"
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
  - "CS1657"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1657"
ms.assetid: 6f0aeebe-5c90-4d5b-981c-1795d2e8fbb9
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1657
无法将“parameter”作为 ref 或 out 参数进行传递，原因是“reason”  
  
 如果在某个变量是只读变量的上下文将该变量作为 [ref](/dotnet/csharp/language-reference/keywords/ref) 或 [out](/dotnet/csharp/language-reference/keywords/out) 参数进行传递，则会发生此错误。 只读上下文包括 [foreach](/dotnet/csharp/language-reference/keywords/foreach-in) 迭代变量、[using](/dotnet/csharp/language-reference/keywords/using-statement) 变量和 `fixed` 变量。 要解决此错误，请勿调用在 `using` 块、`foreach` 语句和 `fixed` 语句中采用 `foreach`、`using` 或 `fixed` 变量作为 `ref` 或 `out` 参数的函数。  
  
## 示例  
 下面的示例生成 CS1657：  
  
```  
// CS1657.cs using System; class C : IDisposable { public int i; public void Dispose() {} } class CMain { static void f(ref C c) { } static void Main() { using (C c = new C()) { f(ref c);  // CS1657 } } }  
```  
  
## 示例  
 下面的代码演示 `fixed` 语句中的相同问题：  
  
```  
// CS1657b.cs // compile with: /unsafe unsafe class C { static void F(ref int* p) { } static void Main() { int[] a = new int[5]; fixed(int* p = a) F(ref p); // CS1657 } }  
```