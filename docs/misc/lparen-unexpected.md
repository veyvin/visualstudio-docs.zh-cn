---
title: "意外的“(” | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc32095"
  - "bc32095"
helpviewer_keywords: 
  - "BC32095"
ms.assetid: a47ad15a-2cfc-4d17-9012-27ba85b7d783
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 意外的“(”
意外的“\(”。 不允许非实例化泛型类型的数组。  
  
 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 无法编译数组，除非该数组具有特定数据类型。 不能使用泛型类型的数据类型参数作为数组的数据类型。  
  
 **错误 ID：**BC32095  
  
### 更正此错误  
  
-   如果需要使用数组，则必须将其声明为特定数据类型。 不能使用数据类型参数。  
  
-   如果需要将提供给数据类型参数的数据类型的一组元素，则你必须使用集合而不是数组。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [NIB Visual Basic 中的集合](http://msdn.microsoft.com/zh-cn/8b2b7845-2251-4573-8dd3-c9f9c0a66a21)   
 [在 Visual Basic 中管理对象组](http://msdn.microsoft.com/zh-cn/50be4910-4732-4d5f-a18a-055a162e9037)