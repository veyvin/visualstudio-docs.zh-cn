---
title: "类型“&lt;typename&gt;”和分部类型“&lt;typename&gt;”在容器“&lt;containername&gt;”中冲突，但由于其中一个被声明为“Partial”，因此正在合并 | Microsoft Docs"
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
  - "bc40046"
  - "vbc40046"
helpviewer_keywords: 
  - "BC40046"
ms.assetid: c243e70b-ecd5-49ef-a260-a7bb12a4a3b1
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 类型“&lt;typename&gt;”和分部类型“&lt;typename&gt;”在容器“&lt;containername&gt;”中冲突，但由于其中一个被声明为“Partial”，因此正在合并
类或结构出现在相同容器类型的多个定义中，并且多个定义未标记 `Partial`。  
  
 你必须至少在类或结构的多个定义中的一个上使用 [分部](/dotnet/visual-basic/language-reference/modifiers/partial) 关键字，但是建议你将其用于所有分部定义。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的信息，请参见 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC40046  
  
### 更正此错误  
  
-   在类或结构的每个分部定义中使用 [分部](/dotnet/visual-basic/language-reference/modifiers/partial) 关键字。  
  
## 请参阅  
 [分部](/dotnet/visual-basic/language-reference/modifiers/partial)