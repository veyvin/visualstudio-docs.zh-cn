---
title: "编译器错误 CS0653 | Microsoft Docs"
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
  - "CS0653"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0653"
ms.assetid: c94043b9-b5d9-4294-921d-a4aead124d44
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0653
无法应用特性类“类”，因为它是抽象的  
  
 [抽象的](/dotnet/csharp/language-reference/keywords/abstract)自定义特性类不能用作特性。  
  
 下面的示例生成 CS0653:  
  
```  
// CS0653.cs using System; public abstract class MyAttribute : Attribute { } public class My2Attribute : MyAttribute { } [My]   // CS0653 // try the following line instead // [My2] class MyClass { public static void Main() { } }  
```