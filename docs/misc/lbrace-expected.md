---
title: "应有“{” | Microsoft Docs"
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
  - "vbc30987"
  - "bc30987"
helpviewer_keywords: 
  - "BC30987"
ms.assetid: 3d1552b6-338a-47cf-84d5-77b59209e0d3
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 应有“{”
若要使用对象初始值设定项声明命名类型或匿名类型的实例，必须将字段或属性及其初始值列表括在大括号（{ 和 }）中。  
  
```  
Dim client As New Customer() With {.Name = "Microsoft", .City = "Seattle"}  
Dim emp = New Employee() With {.Name = "Rob Young", .ID = 55555}  
Dim anon = New With {.ID = 123456}  
```  
  
 **错误 ID：**BC30987  
  
### 更正此错误  
  
-   在 `With` 之后的大括号内包括初始化列表。  
  
## 请参阅  
 [对象初始值设定项：命名类型和匿名类型](../Topic/Object%20Initializers:%20Named%20and%20Anonymous%20Types%20\(Visual%20Basic\).md)   
 [不在生成中：属性过程与字段](http://msdn.microsoft.com/zh-cn/da1c05c1-87c7-40fa-b92c-e9c7e4d170f7)   
 [匿名类型](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types)