---
title: "编译器错误 CS1617 | Microsoft Docs"
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
  - "CS1617"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1617"
ms.assetid: fd3371ed-39eb-4d3d-b8f5-d96ac0c79398
caps.latest.revision: 10
caps.handback.revision: 10
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1617
\/langversion 的选项“option”无效；必须是 ISO\-1、ISO\-2 或默认值  
  
 如果使用 [\/langversion](/dotnet/csharp/language-reference/compiler-options/langversion-compiler-option) 命令行开关或项目设置，但未指定有效的语言选项，则会发生此错误。 若要解决此错误，请检查命令行语法或项目设置并将其更改为其中一个列出的选项。  
  
 例如，用 `csc /langversion:ISO` 编译将生成错误 CS1617。