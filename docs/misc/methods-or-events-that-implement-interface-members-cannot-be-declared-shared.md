---
title: "实现接口成员的方法或事件不能声明为“Shared” | Microsoft Docs"
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
  - "bc30505"
  - "vbc30505"
helpviewer_keywords: 
  - "BC30505"
ms.assetid: a24937c5-aeac-47de-a08b-d8696dd8221a
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 实现接口成员的方法或事件不能声明为“Shared”
已尝试声明为实现接口成员的 `Shared` 方法或事件。 不能将类中实现的方法和事件指定为 `Shared` 或 `Private`，非可继承的类除外。  
  
 **错误 ID：**BC30505  
  
### 更正此错误  
  
-   删除 `Shared` 关键字。  
  
## 请参阅  
 [Shared](/dotnet/visual-basic/language-reference/modifiers/shared)