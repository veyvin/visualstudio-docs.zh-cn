---
title: "不能在 lambda 表达式的参数名中指定数组修饰符，只能在其类型中指定 | Microsoft Docs"
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
  - "vbc36643"
  - "bc36643"
helpviewer_keywords: 
  - "BC36643"
ms.assetid: 34b6141b-6eab-4641-a3f4-53ef28c1792b
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 不能在 lambda 表达式的参数名中指定数组修饰符，只能在其类型中指定
可以将数组参数发送到 lambda 表达式，但参数声明必须包括元素类型。  
  
```vb#  
' Not valid.  
' Dim arrayExample1 = Function(arrayPara()) 2  
  
' Valid.  
Dim arrayExample2 = Function(arrayPara() As Integer) arrayPara.Length > 0  
Dim arrayexample3 = Function(arrayPara As Integer()) arrayPara.Length > 0  
```  
  
 **错误 ID：**BC36643  
  
### 更正此错误  
  
-   指定数组参数中元素的类型。  
  
## 请参阅  
 [lambda 表达式](/dotnet/visual-basic/programming-guide/language-features/procedures/lambda-expressions)