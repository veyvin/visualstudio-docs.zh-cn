---
title: "编译器错误 CS0503 | Microsoft Docs"
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
  - "CS0503"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0503"
ms.assetid: 12a337c9-8c5d-473d-8ce6-057b2c7e7935
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0503
抽象方法“method”不能标记为 virtual  
  
 将成员方法同时标记为 [abstract](/dotnet/csharp/language-reference/keywords/abstract) 和 [virtual](/dotnet/csharp/language-reference/keywords/virtual) 的做法是多余的，因为 **abstract** 意味着**virtual**。  
  
 下面的示例生成 CS0503：  
  
```  
// CS0503.cs namespace x { abstract public class clx { abstract virtual public void f();   // CS0503 } }  
```