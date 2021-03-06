---
title: "来自“implements &lt;derivedinterfacename&gt;”的“&lt;baseinterfacename&gt;.&lt;membername&gt;”已由基类“&lt;baseclassname&gt;”实现。 假定重新实现 &lt;type&gt;。 | Microsoft Docs"
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
  - "bc42014"
  - "vbc42014"
helpviewer_keywords: 
  - "BC42014"
ms.assetid: 95fff622-5d54-4ec8-90f0-477de1d58687
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 来自“implements &lt;derivedinterfacename&gt;”的“&lt;baseinterfacename&gt;.&lt;membername&gt;”已由基类“&lt;baseclassname&gt;”实现。 假定重新实现 &lt;type&gt;。
派生类中的属性、过程或事件使用 `Implements` 子句，用于指定已在基类中的基接口上实现的派生接口成员。  
  
 所实现的成员由基接口定义并由派生接口继承。 基类直接实现基接口。 派生类实现派生接口，可能容易忽视基类已实现了成员这一事实。  
  
 派生类可以重新实现由其基类实现的接口成员。 这与重写基类实现不同。 有关详细信息，请参阅[Implements](/dotnet/visual-basic/language-reference/statements/implements-clause)。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的信息，请参见 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC42014  
  
### 更正此错误  
  
-   如果要重新实现接口成员，则无需执行任何操作。 派生类中的代码可访问重新实现的成员，除非使用 [MyBase \- delete](http://msdn.microsoft.com/zh-cn/52491d06-6451-4f6f-9aa6-8fab59bbc2b9) 关键字访问基类实现。  
  
-   如果不打算重新实现接口成员，请从属性、过程或事件声明中删除 `Implements` 子句。  
  
## 请参阅  
 [接口](/dotnet/visual-basic/programming-guide/language-features/interfaces/index)   
 [不在生成中：Implements 关键字和 Implements 语句](http://msdn.microsoft.com/zh-cn/b96560f7-6413-480f-a1e2-f80253bab5be)