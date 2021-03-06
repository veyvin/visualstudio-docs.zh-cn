---
title: "Lambda 参数“&lt;参数&gt;”隐藏封闭块中的变量、以前定义的范围变量或者查询表达式中隐式声明的变量。 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc36641"
  - "vbc36641"
helpviewer_keywords: 
  - "BC36641"
ms.assetid: ee08c366-29d1-4abb-b14c-23ae2b9680e7
caps.latest.revision: 3
caps.handback.revision: 3
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Lambda 参数“&lt;参数&gt;”隐藏封闭块中的变量、以前定义的范围变量或者查询表达式中隐式声明的变量。
Lambda 表达式中的变量与之前在同个作用域内定义的变量同名。 这可以是位于嵌套的 lambda 表达式代码的封闭块中的变量，可以是 LINQ 查询中之前定义的范围变量或者是 LINQ 查询的隐式声明的变量。  
  
 **错误 ID：**BC36641  
  
### 更正此错误  
  
-   确保在 lambda 表达式中的所有变量都具有唯一名称，该名称不能与同一作用域中已有变量名称重复。  
  
## 请参阅  
 [lambda 表达式](/dotnet/visual-basic/programming-guide/language-features/procedures/lambda-expressions)   
 [Visual Basic 中的 LINQ 简介](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)   
 [LINQ](/dotnet/visual-basic/programming-guide/language-features/linq/index)