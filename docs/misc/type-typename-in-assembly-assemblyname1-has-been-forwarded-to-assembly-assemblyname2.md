---
title: "程序集“&lt;assemblyname1&gt;”中的类型“&lt;typename&gt;”已被转发给程序集“&lt;assemblyname2&gt;” | Microsoft Docs"
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
  - "vbc31424"
  - "bc31424"
helpviewer_keywords: 
  - "BC31424"
  - "类型转发"
ms.assetid: 0f53e613-c1cb-4722-acb5-afa3091e277b
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 程序集“&lt;assemblyname1&gt;”中的类型“&lt;typename&gt;”已被转发给程序集“&lt;assemblyname2&gt;”
程序集“\<assemblyname1\>”中的类型“\<typename\>”已被转发给程序集“\<assemblyname2\>”。 你的项目中缺少对“\<assemblyname2\>”的引用或者程序集“\<assemblyname2\>”中缺少类型“\<typename\>”。  
  
 程序集源代码中的表达式引用已被转发给另一个程序集的类型，但在目标程序集中找不到该类型。  
  
 *“类型转发”*指的是对程序集重新分配类、结构、接口、委托或枚举的定义，但最初已定义的程序集除外。 它通常结合*“代码重构”*使用，这样你可以将一个程序集拆分为两个或多个程序集，或者将代码从一个程序集移到另一个程序集。  
  
 尽管在原始程序集中类型暂时仍然可用，但当代码重构将其从原始程序集删除后，其将变成未定义。  
  
 **错误 ID：**BC31424  
  
### 更正此错误  
  
-   确保目标程序集中存在该类型。  
  
-   确保你的项目具有对目标程序集的引用。  
  
## 请参阅  
 <xref:System.Runtime.CompilerServices.TypeForwardedToAttribute>   
 [类型转发 \(C\+\+\/CLI\)](/visual-cpp/windows/type-forwarding-cpp-cli)   
 [管理项目中的引用](../ide/managing-references-in-a-project.md)   
 [NIB 如何：使用“添加引用”对话框添加或删除引用](http://msdn.microsoft.com/zh-cn/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)