---
title: "不能在包含“As New”的变量声明中指定可为 null 的修饰符 | Microsoft Docs"
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
  - "bc33109"
  - "vbc33109"
helpviewer_keywords: 
  - "BC33109"
ms.assetid: 135def20-3535-4239-bffb-43208d1b3f63
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 不能在包含“As New”的变量声明中指定可为 null 的修饰符
可为 null 的类型修饰符 \(?\) 已包含在已指定 `As New` 的变量声明中。 以下示例会导致此错误：  
  
```vb#  
Dim num? As New ExampleStructure  
```  
  
 **错误 ID：**BC33109  
  
### 更正此错误  
  
1.  从可为 null 的变量声明中删除 `New` 关键字，如下面的示例中所示：  
  
    ```vb#  
    Dim num? As ExampleStructure  
    ```  
  
## 请参阅  
 [可以为 Null 的值类型](/dotnet/visual-basic/programming-guide/language-features/data-types/nullable-value-types)