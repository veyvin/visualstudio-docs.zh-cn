---
title: "&lt;type1&gt;“&lt;typename1&gt;”与为&lt;type2&gt;“&lt;typename2&gt;”中的“&lt;eventname&gt;”事件隐式声明的成员冲突 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc31061"
  - "bc31061"
helpviewer_keywords: 
  - "BC31061"
ms.assetid: de5b1121-8c8f-4aba-a3e7-1e3e60df0dc5
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;type1&gt;“&lt;typename1&gt;”与为&lt;type2&gt;“&lt;typename2&gt;”中的“&lt;eventname&gt;”事件隐式声明的成员冲突
类型成员名称与为事件隐式创建的成员名称冲突。 事件隐式创建多个隐式变量。 例如，声明 `Event X` 隐式声明了名称 `XEventHandler`、`XEvent`、`add_X` 和 `remove_X`。  
  
 **错误 ID：**BC31061  
  
### 更正此错误  
  
-   重命名显式声明的成员，以消除命名冲突。  
  
## 请参阅  
 [NotInBuild：Visual Basic 中的声明语句](http://msdn.microsoft.com/zh-cn/81f3c398-f45c-4d95-80bf-aa39d1a0fb30)   
 [事件](/dotnet/visual-basic/programming-guide/language-features/events/events)