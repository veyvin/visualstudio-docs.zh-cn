---
title: "为类“&lt;classname&gt;”指定了“Microsoft.VisualBasic.ComClassAttribute”，但该类没有可以向 COM 公开的公共成员；因此不生成 COM 接口 | Microsoft Docs"
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
  - "bc40011"
  - "vbc40011"
helpviewer_keywords: 
  - "BC40011"
ms.assetid: 39aed273-bf27-4667-8116-022c4dd8f3c5
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 为类“&lt;classname&gt;”指定了“Microsoft.VisualBasic.ComClassAttribute”，但该类没有可以向 COM 公开的公共成员；因此不生成 COM 接口
使用 `COMClassAttribute` 特性块的类未定义任何 `Public` 特性或方法。 如果要将某个类公开为 COM 对象，必须使用 `Public` 访问权限来声明其属性和方法。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的详细信息，请参见 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC40011  
  
### 更正此错误  
  
-   向类中的一个或多个特性或方法添加 `Public` 关键字，或删除 `COMClassAttribute` 特性块。  
  
## 请参阅  
 [不在生成中：Visual Basic 中使用的特性](http://msdn.microsoft.com/zh-cn/22231318-8a40-49af-9245-e0aab723563b)   
 [不在生成中：特性的应用程序](http://msdn.microsoft.com/zh-cn/2b1703ed-4437-49b3-bc0b-568094324f47)   
 [Public](/dotnet/visual-basic/language-reference/modifiers/public)   
 [ComClassAttribute 类](http://msdn.microsoft.com/zh-cn/5c2f0835-9210-47dc-bc59-5c1769953574)