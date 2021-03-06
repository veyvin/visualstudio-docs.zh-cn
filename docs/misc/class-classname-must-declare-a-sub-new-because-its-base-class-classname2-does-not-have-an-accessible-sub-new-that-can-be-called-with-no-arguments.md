---
title: "类“&lt;classname&gt;”必须声明一个“Sub New”，原因是它的基类“&lt;classname2&gt;”没有不使用参数就可以调用的可访问“Sub New”。 | Microsoft Docs"
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
  - "vbc30387"
  - "bc30387"
helpviewer_keywords: 
  - "BC30387"
ms.assetid: ff587e79-fa47-4b55-9a08-24688b209e0a
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 类“&lt;classname&gt;”必须声明一个“Sub New”，原因是它的基类“&lt;classname2&gt;”没有不使用参数就可以调用的可访问“Sub New”。
派生的类没有声明构造函数，且由于没有可调用的基类构造函数，因此 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 不能生成构造函数。  
  
 当派生的类没有声明构造函数时，[!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 尝试生成一个调用 `MyBase.New()` 的隐式无参数构造函数。 如果基类中没有无需参数即可调用的可访问的构造函数，或者如果有多个，则 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 无法生成隐式构造函数。  
  
 **错误 ID：**BC30387  
  
### 更正此错误  
  
1.  声明和实现派生类中某个位置的至少一个 `Sub New` 构造函数。  
  
2.  添加对基类构造函数 `MyBase.New()` 的调用，作为每个 `Sub New` 的第一行。  
  
## 请参阅  
 [对象生存期：如何创建和销毁对象](../Topic/Object%20Lifetime:%20How%20Objects%20Are%20Created%20and%20Destroyed%20\(Visual%20Basic\).md)   
 [不在生成中：使用构造函数和析构函数](http://msdn.microsoft.com/zh-cn/548eebe1-86c4-4377-b2f5-447cb8be3d90)   
 [Optional](/dotnet/visual-basic/language-reference/modifiers/optional)   
 [ParamArray](/dotnet/visual-basic/language-reference/modifiers/paramarray)   
 [可选参数](/dotnet/visual-basic/programming-guide/language-features/procedures/optional-parameters)   
 [参数数组](/dotnet/visual-basic/programming-guide/language-features/procedures/parameter-arrays)