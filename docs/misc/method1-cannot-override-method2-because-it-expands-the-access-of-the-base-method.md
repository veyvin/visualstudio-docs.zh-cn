---
title: "“&lt;方法1&gt;”无法替代“&lt;方法2&gt;”，因为它扩展了基方法的访问权限 | Microsoft Docs"
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
  - "vbc32203"
  - "bc32203"
helpviewer_keywords: 
  - "BC32203"
ms.assetid: ef7816a4-5f57-4346-80fc-9311bc150b6b
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;方法1&gt;”无法替代“&lt;方法2&gt;”，因为它扩展了基方法的访问权限
过程指定了 `Overrides`，但声明可访问性受到的限制少于将被重写的方法。 不能扩展可访问性，即你不能使重写的方法比被重写的方法更易于访问。 例如，如果基类方法是 `Protected`，则不能用 `Public` 方法重写此方法。  
  
 **错误 ID：**BC32203  
  
### 更正此错误  
  
-   删除 `Overrides` 关键字或更改可访问性，使其至少与基类方法具有同等限制。  
  
## 请参阅  
 [不在生成中：重写属性和方法](http://msdn.microsoft.com/zh-cn/2167e8f5-1225-4b13-9ebd-02591ba90213)   
 [Visual Basic 中的访问级别](/dotnet/visual-basic/programming-guide/language-features/declared-elements/access-levels)   
 [Visual Basic 中的隐藏](/dotnet/visual-basic/programming-guide/language-features/declared-elements/shadowing)