---
title: "由“DefaultEvent”特性指定的“&lt;eventname&gt;”事件不是该类的公共可访问事件。 | Microsoft Docs"
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
  - "vbc30770"
  - "bc30770"
helpviewer_keywords: 
  - "BC30770"
ms.assetid: 7524fba7-2a37-4bc3-b789-87d73a166575
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 由“DefaultEvent”特性指定的“&lt;eventname&gt;”事件不是该类的公共可访问事件。
<xref:System.ComponentModel.DefaultEventAttribute> 特性必须指定应用了该特性的类中可公开访问的事件的名称。  
  
 **错误 ID：**BC30770  
  
### 更正此错误  
  
1.  确保该类定义一个可公开访问的事件。  
  
2.  确保类中事件的名称与 <xref:System.ComponentModel.DefaultEventAttribute> 特性所指定的名称相匹配。  
  
## 请参阅  
 <xref:System.ComponentModel.DefaultEventAttribute>   
 [Event 语句](/dotnet/visual-basic/language-reference/statements/event-statement)   
 [Class 语句](/dotnet/visual-basic/language-reference/statements/class-statement)   
 [Public](/dotnet/visual-basic/language-reference/modifiers/public)