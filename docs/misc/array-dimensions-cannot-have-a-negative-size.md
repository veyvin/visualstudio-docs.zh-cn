---
title: "数组维数的大小不能为负 | Microsoft Docs"
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
  - "bc30611"
  - "vbc30611"
helpviewer_keywords: 
  - "BC30611"
ms.assetid: e310bd0d-f221-4b02-87f3-02124f4de87c
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 数组维数的大小不能为负
一个或多个指定的数组边界是负数。 仅当使用 \-1 作为上限声明空数组时，才能指定负下标。 这样的数组具有零个元素，但它不为 `Nothing`。  
  
 **错误 ID：**BC30611  
  
### 更正此错误  
  
-   使用负数替换负的数组界限。  
  
## 请参阅  
 [数组](/dotnet/visual-basic/programming-guide/language-features/arrays/index)