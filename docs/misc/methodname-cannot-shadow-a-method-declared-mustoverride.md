---
title: "“&lt;methodname&gt;”不能隐藏声明为“MustOverride”的方法 | Microsoft Docs"
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
  - "vbc31404"
  - "bc31404"
helpviewer_keywords: 
  - "BC31404"
ms.assetid: 3e7bb4a0-14af-46ba-bc62-2234c16f1827
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;methodname&gt;”不能隐藏声明为“MustOverride”的方法
在派生类中声明了带有 `MustOverride` 修饰符的同名属性或方法。  
  
 **错误 ID：**BC31404  
  
### 更正此错误  
  
1.  将 `Overrides` 修饰符添加到派生类中的重写属性或方法。  
  
2.  从基类的属性或方法中删除 `MustOverride` 修饰符。  
  
## 请参阅  
 [MustOverride](/dotnet/visual-basic/language-reference/modifiers/mustoverride)