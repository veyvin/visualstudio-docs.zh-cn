---
title: "强制转换运算符中有语法错误；需要两个用逗号分隔的参数 | Microsoft Docs"
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
  - "vbc30944"
  - "bc30944"
helpviewer_keywords: 
  - "BC30944"
ms.assetid: 1f7ed4a1-6ff5-4836-8424-21618c68ff45
caps.latest.revision: 6
caps.handback.revision: 6
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 强制转换运算符中有语法错误；需要两个用逗号分隔的参数
表达式使用 `CType` 转换函数或 `DirectCast` 或 `TryCast` 转换关键字，但仅提供一个参数。  
  
 `CType`、`DirectCast` 和 `TryCast` 都需要两个参数。 第一个是要转换的表达式，第二个是要将其转换成的数据类型或类类型。  
  
 **错误 ID：**BC30944  
  
### 更正此错误  
  
-   根据要求为转换提供两个参数。  
  
-   如果想要使用特定的 [类型转换函数](/dotnet/visual-basic/language-reference/functions/type-conversion-functions) 之一（如 `CString`），则必须使用该函数名称而不是 `CType`。 这样只需要一个参数。  
  
## 请参阅  
 [CType 函数](/dotnet/visual-basic/language-reference/functions/ctype-function)   
 [DirectCast 运算符](/dotnet/visual-basic/language-reference/operators/directcast-operator)   
 [TryCast 运算符](/dotnet/visual-basic/language-reference/operators/trycast-operator)   
 [类型转换函数](/dotnet/visual-basic/language-reference/functions/type-conversion-functions)