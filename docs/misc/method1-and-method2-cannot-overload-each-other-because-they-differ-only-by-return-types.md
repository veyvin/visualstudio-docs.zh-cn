---
title: "“&lt;method1&gt;”和“&lt;method2&gt;”的差异仅在于返回类型，因此它们无法重载对方 | Microsoft Docs"
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
  - "bc30301"
  - "vbc30301"
helpviewer_keywords: 
  - "BC30301"
ms.assetid: 5adc442b-9671-4d93-add8-42929b1a09b9
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;method1&gt;”和“&lt;method2&gt;”的差异仅在于返回类型，因此它们无法重载对方
已尝试用与前者区别仅在于其返回类型的另一种方法重载某种方法。 在进行重载时，你必须通过它们的参数列表区分方法的任意两个版本；不可使用除参数列表外的任何方式来区分方法。  
  
 **错误 ID：**BC30301  
  
### 更正此错误  
  
-   确保通过参数列表区分方法。  
  
## 请参阅  
 [过程重载](/dotnet/visual-basic/programming-guide/language-features/procedures/procedure-overloading)   
 [重载过程注意事项](/dotnet/visual-basic/programming-guide/language-features/procedures/considerations-in-overloading-procedures)