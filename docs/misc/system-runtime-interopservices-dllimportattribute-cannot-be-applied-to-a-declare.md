---
title: "“System.Runtime.InteropServices.DllImportAttribute”不能应用于“Declare”。 | Microsoft Docs"
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
  - "bc31523"
  - "vbc31523"
helpviewer_keywords: 
  - "BC31523"
ms.assetid: 04c8a14f-9286-4f9a-aad5-a0555e5f09f4
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “System.Runtime.InteropServices.DllImportAttribute”不能应用于“Declare”。
`Declare` 函数已使用了 `DllImportAttribute` 特性。 此特性仅可用于 `Function` 或 `Sub`。  
  
 **错误 ID:** BC31523  
  
### 更正此错误  
  
1.  请从此 `Declare` 语句中删除 `DllImportAttribute` 特性。  
  
## 请参阅  
 <xref:System.Runtime.InteropServices.DllImportAttribute>   
 [Declare 语句](/dotnet/visual-basic/language-reference/statements/declare-statement)