---
title: "“&lt;typename&gt;”不能用作特性，因为它具有未重写的“MustOverride”方法 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc31507"
  - "vbc31507"
helpviewer_keywords: 
  - "BC31507"
ms.assetid: 843643d3-3e81-4ce3-b4df-278882f3954d
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;typename&gt;”不能用作特性，因为它具有未重写的“MustOverride”方法
具有 `MustOverride` 方法的类不能用作特性。  
  
 特性类的 `MustOverride` 成员只能在重写这些成员的派生类中使用。  
  
 **错误 ID：**BC31507  
  
### 更正此错误  
  
1.  从特性类成员中删除 `MustOverride` 修饰符。  
  
2.  在派生类中实现 `MustOverride` 成员，并将此类用作特性。  
  
## 请参阅  
 <xref:System.AttributeUsageAttribute>   
 [不在生成中：Visual Basic 中的自定义特性](http://msdn.microsoft.com/zh-cn/d72d8a5c-8f64-4614-b15b-cad66845d047)