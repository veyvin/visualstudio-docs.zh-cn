---
title: "编译器错误 CS0061 | Microsoft Docs"
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
  - "CS0061"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0061"
ms.assetid: 8dfc57a9-653d-4902-a88c-92032ba64024
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0061
可访问性不一致：基接口“interface 1”的可访问性低于接口“interface 2”  
  
 [公共](/dotnet/csharp/language-reference/keywords/public)构造必须返回可以公开访问的对象。  
  
 派生接口中不能收缩接口的可访问性。 有关详细信息，请参阅[接口](/dotnet/csharp/programming-guide/interfaces/index)和[访问修饰符](/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers)。  
  
 以下示例生成 CS0061。  
  
```  
// CS0061.cs // compile with: /target:library internal interface A {} public interface AA : A {}  // CS0061 // OK public interface B {} internal interface BB : B {} internal interface C {} internal interface CC : C {}  
```