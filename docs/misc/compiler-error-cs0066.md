---
title: "编译器错误 CS0066 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0066"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0066"
ms.assetid: 9b50b49b-78b8-4562-8839-d59e5edbec6b
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0066
“event”: 事件必须是委托类型  
  
 事件关键字需要[委托](/dotnet/csharp/language-reference/keywords/delegate)类型。 有关详细信息，请参阅[事件](/dotnet/csharp/programming-guide/events/index)和[委托](/dotnet/csharp/programming-guide/delegates/index)。  
  
 下面的示例生成 CS0066：  
  
```  
// CS0066.cs using System; public class EventHandler { } // to fix the error, remove the event declaration and the // EventHandler class declaration, and uncomment the following line // public delegate void EventHandler(); public class a { public event EventHandler Click;   // CS0066 private void TestMethod() { if (Click != null) Click(); } public static void Main() { } }  
```