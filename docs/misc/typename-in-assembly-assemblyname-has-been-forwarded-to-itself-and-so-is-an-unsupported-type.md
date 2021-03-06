---
title: "程序集“&lt;assemblyname&gt;”中的“&lt;typename&gt;”已转发给自身，因此它是一种不受支持的类型 | Microsoft Docs"
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
  - "bc31425"
  - "vbc31425"
helpviewer_keywords: 
  - "BC31425"
  - "类型转发"
ms.assetid: e3275d55-3f4c-4bbc-9c8f-f55c4e973063
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 程序集“&lt;assemblyname&gt;”中的“&lt;typename&gt;”已转发给自身，因此它是一种不受支持的类型
程序集使用 <xref:System.Runtime.CompilerServices.TypeForwardedToAttribute> 将它的某个类型转发给另一个程序集，但在同一程序集中指定了相同的类型。  
  
 *“类型转发”*指的是对程序集重新分配类、结构、接口、委托或枚举的定义，但最初已定义的程序集除外。 它通常结合*“代码重构”*使用，这样你可以将一个程序集拆分为两个或多个程序集，或者将代码从一个程序集移到另一个程序集。  
  
 将类型转发到其自身会导致循环转发。 如果其他程序集尝试访问已转发的类型，则它会进行无休止的转发，而不会到达尚未转发的类型。  
  
 **错误 ID：**BC31425  
  
### 更正此错误  
  
-   将类型转发给其他程序集中的类型，或根本不进行转发。  
  
## 请参阅  
 <xref:System.Runtime.CompilerServices.TypeForwardedToAttribute>   
 [类型转发 \(C\+\+\/CLI\)](/visual-cpp/windows/type-forwarding-cpp-cli)   
 [管理项目中的引用](../ide/managing-references-in-a-project.md)   
 [NIB 如何：使用“添加引用”对话框添加或删除引用](http://msdn.microsoft.com/zh-cn/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)