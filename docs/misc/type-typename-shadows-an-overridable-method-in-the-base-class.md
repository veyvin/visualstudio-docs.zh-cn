---
title: "&lt;类型&gt;“&lt;类型名称&gt;”隐藏基类中的可重写方法 | Microsoft Docs"
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
  - "vbc40005"
  - "bc40005"
helpviewer_keywords: 
  - "BC40005"
ms.assetid: 1dadda7f-1d26-4ae8-a668-9f69d55ceb50
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;类型&gt;“&lt;类型名称&gt;”隐藏基类中的可重写方法
\<类型\>“\<类型名称\>”隐藏基类中的可重写方法。 若要重写基方法，必须将此方法声明为“Overrides”。  
  
 以基类中定义的重写过程或属性的相同名称来定义编程元素。 在这种情况下，此类中的元素应隐藏基类元素。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的详细信息，请参阅 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC40005  
  
### 更正此错误  
  
-   如果想要重写基过程，将 `Overrides` 关键字添加到声明。  
  
-   如果想要隐藏基过程，将 `Shadows` 关键字添加到声明。  
  
-   如果不想重写或隐藏，则更改正在声明的元素的名称。  
  
## 请参阅  
 [不在生成中：重写属性和方法](http://msdn.microsoft.com/zh-cn/2167e8f5-1225-4b13-9ebd-02591ba90213)   
 [Visual Basic 中的隐藏](/dotnet/visual-basic/programming-guide/language-features/declared-elements/shadowing)   
 [Overrides](/dotnet/visual-basic/language-reference/modifiers/overrides)   
 [Shadows](/dotnet/visual-basic/language-reference/modifiers/shadows)