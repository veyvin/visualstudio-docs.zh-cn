---
title: "匿名类型必须至少包含一个成员 | Microsoft Docs"
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
  - "bc36574"
  - "vbc36574"
helpviewer_keywords: 
  - "BC36574"
ms.assetid: fdc8dd47-ea38-49e8-8dd5-676f726cd101
caps.latest.revision: 5
caps.handback.revision: 5
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 匿名类型必须至少包含一个成员
匿名类型声明中的初始值设定项列表不能为空。  
  
```  
' Not valid. ' Dim anonInstance = New With {}  
```  
  
 **错误 ID：**BC36574  
  
### 更正此错误  
  
-   在大括号内声明成员，如下面的代码中所示。  
  
    ```  
    Dim anonInstance = New With {.MemberName = "value"}  
    ```  
  
## 请参阅  
 [匿名类型](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types)