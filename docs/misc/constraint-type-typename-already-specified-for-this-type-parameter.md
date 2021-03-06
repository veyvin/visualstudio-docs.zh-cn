---
title: "已经为此类型形参指定了约束类型“&lt;typename&gt;” | Microsoft Docs"
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
  - "BC32071"
  - "vbc32071"
helpviewer_keywords: 
  - "BC32071"
ms.assetid: 6b0e85e9-3ac8-4181-97de-ca690b95a63c
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 已经为此类型形参指定了约束类型“&lt;typename&gt;”
约束列表多次包括类或接口约束。  
  
 约束列表对传递给类型形参的类型实参有一定要求。 你可以采用任意组合指定以下要求：  
  
-   该类型实参必须实现一个或多个接口  
  
-   该类型实参最多从一个类继承  
  
 一种类型无法多次实现继承自相同类型，并且不能在相同约束列表中多次指定某种类型。  
  
 **错误 ID：**BC32071  
  
### 更正此错误  
  
-   删除相同类或接口的任何多余指定。 它应仅在约束列表中出现一次。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [类型列表](/dotnet/visual-basic/language-reference/statements/type-list)