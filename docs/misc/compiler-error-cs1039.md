---
title: "编译器错误 CS1039 | Microsoft Docs"
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
  - "CS1039"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1039"
ms.assetid: 266e9f7f-fe17-445a-aefd-6b7795167d68
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1039
字符串未终止  
  
 编译器检测到格式不正确的[字符串](/dotnet/csharp/language-reference/keywords/string)文本。  
  
## 示例  
 下面的示例生成 CS1039。 若要解决此错误，请添加终止引号。  
  
```  
// CS1039.cs public class MyClass { public static void Main() { string b = @"hello, world;   // CS1039 } }  
```