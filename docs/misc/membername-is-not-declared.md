---
title: "未声明“&lt;成员名称&gt;” | Microsoft Docs"
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
  - "vbc30816"
  - "bc30816"
helpviewer_keywords: 
  - "BC30816"
ms.assetid: d6704bed-bb76-47c6-ac28-09608d5e6912
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 未声明“&lt;成员名称&gt;”
未声明“`<membername>`”。`Debug` 对象功能在 `System` 程序集中的 `System.Diagnostics.Debug` 中可用。  
  
 无法找到指定的成员。  
  
 **错误 ID：**BC30816  
  
### 更正此错误  
  
1.  检查成员的拼写。  
  
2.  使用 `Imports` 语句或完全限定在其他命名空间中定义的成员。 例如，在 `System.Diagnostics.Debug` 命名空间中声明 `WriteLine` 函数。  
  
## 请参阅  
 [使用 Visual Studio 进行调试](../debugger/debugging-in-visual-studio.md)