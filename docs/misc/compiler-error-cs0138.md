---
title: "编译器错误 CS0138 | Microsoft Docs"
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
  - "CS0138"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0138"
ms.assetid: 970545f8-5ee5-428e-921a-3aa29f68d16d
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0138
using 命名空间指令只能应用于命名空间；“type”是一个类型，而不是命名空间  
  
 [using](/dotnet/csharp/language-reference/keywords/using) 指令只能采用命名空间的名称作为参数。 有关详细信息，请参阅[命名空间](/dotnet/csharp/programming-guide/namespaces/index)。  
  
 下面的示例生成 CS0138：  
  
```  
// CS0138.cs using System.Object;   // CS0138  
```