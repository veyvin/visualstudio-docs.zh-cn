---
title: "编译器错误 CS1536 | Microsoft Docs"
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
  - "CS1536"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1536"
ms.assetid: 65f14fbb-df79-4759-8911-93f8f90f5a60
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1536
参数类型 void 无效  
  
 不需要指定除 void 指针以外的 [void](/dotnet/csharp/language-reference/keywords/void) 参数或指定无效。  
  
 下面的示例生成 CS1536：  
  
```  
// CS1536.cs class a { public static int x( void )   // CS1536 // try the following line instead // public static int x() { return 0; } public static void Main() { } }  
```