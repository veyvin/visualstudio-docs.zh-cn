---
title: "编译器错误 CS0261 | Microsoft Docs"
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
  - "CS0261"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0261"
ms.assetid: c2af7b31-4a48-457a-8d9b-0956dd0d46f9
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0261
“type”的分部声明必须是所有的类、所有的结构或所有的接口  
  
 如果将分部类型声明为不同位置中构造的不同类型，将发生此错误。 有关详细信息，请参阅[分部类和方法](/dotnet/csharp/programming-guide/classes-and-structs/partial-classes-and-methods)。  
  
 以下示例生成 CS0261：  
  
```  
// CS0261.cs partial class A  // CS0261 – A declared as a class here, but as a struct below { } partial struct A { }  
```