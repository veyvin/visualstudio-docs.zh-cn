---
title: "即使参数值相同，也不能在此项目中多次指定特性“&lt;attributename&gt;” | Microsoft Docs"
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
  - "bc41000"
  - "vbc41000"
helpviewer_keywords: 
  - "BC41000"
ms.assetid: 7e846177-7b89-44da-8f17-cdc8606ef148
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 即使参数值相同，也不能在此项目中多次指定特性“&lt;attributename&gt;”
在同一个编程元素上多次指定了某个自定义特性，但对该自定义特性应用了 <xref:System.AttributeUsageAttribute>，并将其 <xref:System.AttributeUsageAttribute.AllowMultiple%2A> 属性设置为了 `False`。<xref:System.AttributeUsageAttribute.AllowMultiple%2A> 控制该特性是否为多用途特性。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的信息，请参见 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC41000  
  
### 更正此错误  
  
-   删除自定义特性的额外规范，或者，在应用于它的 <xref:System.AttributeUsageAttribute> 中将 <xref:System.AttributeUsageAttribute.AllowMultiple%2A> 设置为 `True`。  
  
## 请参阅  
 <xref:System.AttributeUsageAttribute>   
 <xref:System.AttributeUsageAttribute.AllowMultiple%2A>   
 [不在生成中：特性的应用程序](http://msdn.microsoft.com/zh-cn/2b1703ed-4437-49b3-bc0b-568094324f47)