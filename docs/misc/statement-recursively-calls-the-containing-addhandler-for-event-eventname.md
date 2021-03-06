---
title: "语句递归调用事件“&lt;eventname&gt;”的包含“AddHandler” | Microsoft Docs"
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
  - "bc41998"
  - "vbc41998"
helpviewer_keywords: 
  - "BC41998"
ms.assetid: 4375b191-fbd9-4e93-b9bb-9159d533ddf6
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 语句递归调用事件“&lt;eventname&gt;”的包含“AddHandler”
事件定义的 `AddHandler` 访问器中的语句不能直接引用该事件。  
  
 建议的方法是将事件的处理程序列表存储为定义该事件的类、结构或模块中的私有字段。 有关详细信息，请参阅[如何：声明自定义事件以避免阻止](../Topic/How%20to:%20Declare%20Custom%20Events%20To%20Avoid%20Blocking%20\(Visual%20Basic\).md)和[如何：声明自定义事件以节省内存](../Topic/How%20to:%20Declare%20Custom%20Events%20To%20Conserve%20Memory%20\(Visual%20Basic\).md)。  
  
 **错误 ID：**BC41998  
  
### 更正此错误  
  
-   重写事件定义以避免递归。  
  
## 请参阅  
 [AddHandler \- delete](http://msdn.microsoft.com/zh-cn/fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [Event 语句](/dotnet/visual-basic/language-reference/statements/event-statement)   
 [如何：声明自定义事件以避免阻止](../Topic/How%20to:%20Declare%20Custom%20Events%20To%20Avoid%20Blocking%20\(Visual%20Basic\).md)   
 [如何：声明自定义事件以节省内存](../Topic/How%20to:%20Declare%20Custom%20Events%20To%20Conserve%20Memory%20\(Visual%20Basic\).md)