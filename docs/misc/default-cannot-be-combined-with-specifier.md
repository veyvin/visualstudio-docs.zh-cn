---
title: "“Default”不能与“&lt;specifier&gt;”组合 | Microsoft Docs"
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
  - "vbc30490"
  - "bc30490"
helpviewer_keywords: 
  - "BC30490"
ms.assetid: fb29622c-a176-4185-94ae-2c1ca85adddb
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “Default”不能与“&lt;specifier&gt;”组合
试图将 `Default` 关键字与此上下文中无效的说明符（例如 `Shared` 或 `Private`组合起来。  
  
 **错误 ID：**BC30490  
  
### 更正此错误  
  
-   删除 `Default`。  
  
     \- 或 \-  
  
-   删除冲突的说明符。  
  
## 请参阅  
 [Default](/dotnet/visual-basic/language-reference/modifiers/default)