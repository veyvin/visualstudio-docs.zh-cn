---
title: "结构方法内部的局部变量不能声明为 &quot;Static&quot; | Microsoft Docs"
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
  - "vbc31400"
  - "bc31400"
helpviewer_keywords: 
  - "BC31400"
ms.assetid: 38b8adee-3593-40fb-b0a4-e2a47599567f
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 结构方法内部的局部变量不能声明为 &quot;Static&quot;
不能将 `Static` 修饰符用于结构中的局部变量。  
  
 **错误 ID：**BC31400  
  
### 更正此错误  
  
1.  从局部变量中删除 `Static` 修饰符。  
  
2.  将该变量声明为具有扩大范围的静态变量。  
  
## 请参阅  
 [Static](/dotnet/visual-basic/language-reference/modifiers/static)