---
title: "编译器错误 CS0737 | Microsoft Docs"
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
  - "CS0737"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0737"
ms.assetid: d2247770-5546-46f2-a01d-8e2ebfcbb859
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0737
“type name”不实现接口成员“member name”。 “method name”无法实现接口成员，因为它不是公共的。  
  
 实现接口成员的方法必须具有公共可访问性。 所有接口成员均为 `public`。  
  
### 更正此错误  
  
1.  向该方法添加 [public](/dotnet/csharp/language-reference/keywords/public) 访问修饰符。  
  
## 示例  
 下面的代码生成 CS0737：  
  
```  
// cs0737.cs interface ITest { // Default access of private with no modifier. int Return42(); // Try the following line instead. // public int Return42(); } struct Struct1 : ITest // CS0737 { int Return42() { return (42); } } public class Test { public static int Main(string[] args) { Struct1 s1 = new Struct1(); return (1); } }  
```  
  
## 请参阅  
 [接口](/dotnet/csharp/programming-guide/interfaces/index)