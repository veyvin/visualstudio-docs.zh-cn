---
title: "“&lt;methodname&gt;”和“&lt;methodname&gt;”无法重载对方，应为它们的差异仅在于“ReadOnly”或“WriteOnly”。 | Microsoft Docs"
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
  - "vbc30366"
  - "BC30366"
helpviewer_keywords: 
  - "BC30366"
ms.assetid: 2440fd29-e205-4004-b2ee-9d954d17b8d3
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;methodname&gt;”和“&lt;methodname&gt;”无法重载对方，应为它们的差异仅在于“ReadOnly”或“WriteOnly”。
试图重载两种方法，它们的差异仅在于 `ReadOnly` 和 `WriteOnly` 声明。 只能使用参数列表内的所有内容来区分版本。  
  
 **错误 ID：**BC30366  
  
### 更正此错误  
  
-   请确保方法由多个 `ReadOnly` 和 `WriteOnly` 区分。  
  
## 请参阅  
 [重载过程注意事项](/dotnet/visual-basic/programming-guide/language-features/procedures/considerations-in-overloading-procedures)