---
title: "“Next”语句命名的变量比已有的匹配“For”语句多 | Microsoft Docs"
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
  - "bc32037"
  - "vbc32037"
helpviewer_keywords: 
  - "BC32037"
ms.assetid: 7c97d835-1043-40ec-a645-63a053f5f916
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “Next”语句命名的变量比已有的匹配“For”语句多
多个嵌套循环由单个 `Next` 语句终止，并且该语句指定的循环变量多于嵌套中的循环数，如下例所示：  
  
```  
For I = 1 To 10 For J = 1 To 5 ' ... Next J, I, K   ' Next J, I is valid, but there is no loop on K.  
```  
  
 **错误 ID：**BC32037  
  
### 更正此错误  
  
1.  确保 `Next` 语句按照与循环开始顺序相反的顺序指定所有嵌套循环变量。  
  
2.  从 `Next` 语句删除中所有外部变量。  
  
## 请参阅  
 [For...Next 语句](/dotnet/visual-basic/language-reference/statements/for-next-statement)