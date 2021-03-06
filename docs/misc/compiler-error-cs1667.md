---
title: "编译器错误 CS1667 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1667"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1667"
ms.assetid: 59f64828-58bc-487c-862a-75537e21d4ea
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1667
特性“attribute”对属性或事件访问器无效。 仅对“declaration type”声明有效。  
  
 如果当特性本身应在属性或事件上时，对该属性或事件访问器使用该特性，会发生此错误。 使用 <xref:System.CLSCompliantAttribute>、<xref:System.Diagnostics.ConditionalAttribute> 和 <xref:System.ObsoleteAttribute> 特性时会发生此错误。  
  
## 示例  
 以下示例生成 CS1670：  
  
```  
// CS1667.cs using System; public class C { private int i; //Try this instead: //[Obsolete] public int ObsoleteProperty { [Obsolete]  // CS1667 get { return i; } set { i = value; } } public static void Main() { } }  
```