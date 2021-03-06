---
title: "为类“&lt;partialclassname&gt;”指定的基类“&lt;baseclassname1&gt;”不能与它的其他分部类型之一的基类“&lt;baseclassname2&gt;”不同 | Microsoft Docs"
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
  - "BC30928"
  - "vbc30928"
helpviewer_keywords: 
  - "BC30928"
ms.assetid: da464f09-1016-4dec-beb7-3202cacd8e1e
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 为类“&lt;partialclassname&gt;”指定的基类“&lt;baseclassname1&gt;”不能与它的其他分部类型之一的基类“&lt;baseclassname2&gt;”不同
在两个或更多分部声明中定义了某个类，这些声明包含多个指定多个基类的 [Inherits 语句](/dotnet/visual-basic/language-reference/statements/inherits-statement)。  
  
 在多个分部声明间划分类的定义时，编译器会将该类视为它的所有分部声明的联合。 这不仅适用于成员，还适用于实现、继承和访问级别。  
  
 一个类可以实现多个接口，但它无法从多个基类中继承。 因此，所有 `Inherits` 语句必须指定相同的基类。  
  
 **错误 ID：**BC30928  
  
### 更正此错误  
  
-   确定哪种类应成为分部类的基类，并从其分部声明中删除任何指定其他基类的 `Inherits` 语句。  
  
## 请参阅  
 [分部](/dotnet/visual-basic/language-reference/modifiers/partial)   
 [Inherits 语句](/dotnet/visual-basic/language-reference/statements/inherits-statement)   
 [继承的基础知识](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)