---
title: "编译器警告（等级 4）CS1573 | Microsoft Docs"
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
  - "CS1573"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1573"
ms.assetid: 1b68cb1a-9bfd-4343-b9b6-8ce195af5e23
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器警告（等级 4）CS1573
参数“parameter”在用于“parameter”的 XML 注释中没有匹配的 param 标记（但其他参数有）  
  
 使用 [\/doc](/dotnet/csharp/language-reference/compiler-options/doc-compiler-option) 编译器选项时，只为某些而非全部方法中的参数指定了注释。 你可能忘记了为这些参数输入注释。  
  
 下面的示例生成 CS1573：  
  
```  
// CS1573.cs // compile with: /W:4 public class MyClass { /// <param name='Int1'>Used to indicate status.</param> // enter a comment for Char1? public static void MyMethod(int Int1, char Char1) { } public static void Main () { } }  
```