---
title: "编译器错误 CS0505 | Microsoft Docs"
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
  - "CS0505"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0505"
ms.assetid: e3cb9e33-7338-4869-859b-81d7439f0d23
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0505
“member1”: 无法重写，因为“member2”不是函数  
  
 类声明已尝试重写基类中的非方法。 重写必须与成员类型相匹配。 如果所需方法的名称要与基类中某方法的名称相同，请在基类的方法声明上使用 [new](/dotnet/csharp/language-reference/keywords/new)（而不是 [override](/dotnet/csharp/language-reference/keywords/override)）。  
  
 下面的示例生成 CS0505：  
  
```  
// CS0505.cs // compile with: /target:library public class clx { public int i; } public class cly : clx { public override int i() { return 0; }   // CS0505 }  
```