---
title: "编译器错误 CS1509 | Microsoft Docs"
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
  - "CS1509"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1509"
ms.assetid: 51a475c3-f085-49cb-89b0-c6582b68653f
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1509
引用的文件“file”不是程序集；请改用“\/addmodule”选项  
  
 在使用 [\/target: module](../Topic/-target:module%20\(C%23%20Compiler%20Options\).md) 的编译中（没有程序集清单）产生的输出文件（输出文件 1）被指定为了 [\/reference](/dotnet/csharp/language-reference/compiler-options/reference-compiler-option)。 因此，不是程序集追加到当前程序的程序集，而是输出文件 1 中的元数据信息将添加到当前程序的程序集。