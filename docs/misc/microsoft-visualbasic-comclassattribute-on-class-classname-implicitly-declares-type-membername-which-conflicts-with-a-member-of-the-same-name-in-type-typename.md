---
title: "“&lt;classname&gt;”类中的“Microsoft.VisualBasic.ComClassAttribute”隐式声明与 &lt;type&gt;“&lt;typename&gt;”中的同名成员发生冲突的 &lt;type&gt; “&lt;membername&gt;” | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "BC42101"
ms.assetid: 001c8eaa-19b6-44fa-8056-4186ecffbda8
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;classname&gt;”类中的“Microsoft.VisualBasic.ComClassAttribute”隐式声明与 &lt;type&gt;“&lt;typename&gt;”中的同名成员发生冲突的 &lt;type&gt; “&lt;membername&gt;”
“\<classname\>”类中的“Microsoft.VisualBasic.ComClassAttribute”隐式声明与 \<type\>“\<typename\>”中的同名成员发生冲突的 \<type\> “\<membername\>”。 如果想要隐藏“\<typename\>”基中的名称，请使用“Microsoft.VisualBasic.ComClassAttribute\(InterfaceShadows:\=True\)”。  
  
 使用 `COMClassAttribute` 特性块的类隐式定义与基类成员同名的接口。 在这种情况下，接口名应隐藏基类成员。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的详细信息，请参见 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC42101  
  
### 更正此错误  
  
1.  如果不打算隐藏基类成员，请在 `ComClassAttribute` 特性块中设置 `InterfaceShadows:=True`。  
  
2.  如果不打算隐藏基类成员，请更改类名称。  
  
## 请参阅  
 [不在生成中：Visual Basic 中使用的特性](http://msdn.microsoft.com/zh-cn/22231318-8a40-49af-9245-e0aab723563b)   
 [不在生成中：特性的应用程序](http://msdn.microsoft.com/zh-cn/2b1703ed-4437-49b3-bc0b-568094324f47)   
 [ComClassAttribute 类](http://msdn.microsoft.com/zh-cn/5c2f0835-9210-47dc-bc59-5c1769953574)   
 [ComClassAttribute.InterfaceShadows 特性](http://msdn.microsoft.com/zh-cn/0fae25bd-e0ba-4755-a76c-3b526b1ac795)