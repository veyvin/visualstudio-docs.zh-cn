---
title: "编译器错误 CS0065 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0065"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0065"
ms.assetid: 49ca30a8-513a-40ed-aa0c-eb696a25b91f
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0065
“event”：事件属性必须同时具有 add 和 remove 访问器  
  
 并不是字段的事件必须有两种访问方法。  
  
 以下示例生成 CS0065：  
  
```  
// CS0065.cs using System; public delegate void Eventhandler(object sender, int e); public class MyClass { public event EventHandler Click   // CS0065, { // to fix, uncomment the add and remove definitions /* add { Click += value; } remove { Click -= value; } */ } public static void Main() { } }  
```  
  
## 请参阅  
 [事件](/dotnet/csharp/programming-guide/events/index)