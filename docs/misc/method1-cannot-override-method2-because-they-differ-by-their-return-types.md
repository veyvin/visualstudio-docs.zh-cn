---
title: "“&lt;method1&gt;”无法重写“&lt;method2&gt;”，因为它们的返回类型不同 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30437"
  - "vbc30437"
helpviewer_keywords: 
  - "BC30437"
ms.assetid: e566ae72-c597-4b33-b70d-5d4ea879d644
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;method1&gt;”无法重写“&lt;method2&gt;”，因为它们的返回类型不同
你已试图使用另一个返回类型不同的方法重写一个方法。 类型可重写继承的可重写方法，方法是声明具有相同名称和签名的方法，并用 `Overrides` 修饰符标记声明。 这两种方法的签名必须匹配。  
  
 **错误 ID：**BC30437  
  
### 更正此错误  
  
-   检查这两种方法的返回类型，并根据匹配需要进行更改。  
  
## 请参阅  
 [不在生成中：重写属性和方法](http://msdn.microsoft.com/zh-cn/2167e8f5-1225-4b13-9ebd-02591ba90213)