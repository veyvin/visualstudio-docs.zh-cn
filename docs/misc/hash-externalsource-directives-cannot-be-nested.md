---
title: "不能嵌套“#ExternalSource”指令 | Microsoft Docs"
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
  - "bc30580"
  - "vbc30580"
helpviewer_keywords: 
  - "BC30580"
ms.assetid: 56c6ef4b-28b1-4a62-8afa-d83a7742b507
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 不能嵌套“#ExternalSource”指令
你已尝试将 `#ExternalSource` 指令放置在另一个 `#ExternalSource` 块内。`#ExternalSource` 指令引用外部代码，使编译器能够在此代码中发生异常时准确地报告。  
  
 `#ExternalSource` 块不能被嵌套在其他 `#ExternalSource` 块内。  
  
 **错误 ID：**BC30580  
  
### 更正此错误  
  
-   将内部 `#ExternalSource` 指令移动到封闭的 `#ExternalSource` 块外部。  
  
## 请参阅  
 [\#ExternalSource 指令](/dotnet/visual-basic/language-reference/directives/externalsource-directive)   
 [NOTINBUILD 条件编译 \(Visual Basic\)](http://msdn.microsoft.com/zh-cn/ad1e35e0-935e-4a35-a2ae-738bcf2a9240)