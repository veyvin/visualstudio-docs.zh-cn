---
title: "编译器警告（等级 1）CS3012 | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS3012"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS3012"
ms.assetid: 1f7555b4-61e4-4821-85c9-586301df4c5c
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器警告（等级 1）CS3012
不能在模块上指定与程序集的 CLSCompliant 特性不同的 CLSCompliant 特性  
  
 为了通过 `[module:System.CLCSompliant(true)]` 使模块符合公共语言规范 \(CLS\)，此模块必须使用 [\/target: module](../Topic/-target:module%20\(C%23%20Compiler%20Options\).md) 编译器选项生成。 有关 CLS 的详细信息，请参见 [语言独立性和与语言无关的组件](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md)。  
  
## 示例  
 当没有使用 `/target:module` 生成时，以下示例将生成 CS3012：  
  
```  
// CS3012.cs // compile with: /W:1 [module:System.CLSCompliant(true)]   // CS3012 public class C { public static void Main() { } }  
```