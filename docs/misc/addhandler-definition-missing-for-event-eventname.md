---
title: "缺少事件“&lt;eventname&gt;”的 &quot;AddHandler&quot; 定义 | Microsoft Docs"
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
  - "bc31130"
  - "vbc31130"
helpviewer_keywords: 
  - "BC31130"
ms.assetid: cf6c7fd6-ce2e-4916-b427-2a4a63e7279d
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 缺少事件“&lt;eventname&gt;”的 &quot;AddHandler&quot; 定义
如果事件被声明为 `Custom`，它必须提供用于添加事件处理程序的过程。  
  
 **错误 ID：**BC31130  
  
### 更正此错误  
  
1.  在 `Custom Event` 语句和 `End Event` 语句之间包含 `AddHandler` 声明。  
  
2.  验证事件声明中的其他过程是否正确终止。  
  
## 请参阅  
 [AddHandler 语句](/dotnet/visual-basic/language-reference/statements/addhandler-statement)   
 [Event 语句](/dotnet/visual-basic/language-reference/statements/event-statement)