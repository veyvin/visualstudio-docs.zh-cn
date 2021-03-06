---
title: "编译器错误 CS0434 | Microsoft Docs"
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
  - "CS0434"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0434"
ms.assetid: 8f8871fc-a4bb-4a9e-ba19-999f4943001e
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0434
NamespaceName2 中的命名空间 NamespaceName1 与 NamespaceName3 中的类型 TypeName1 冲突  
  
 当导入的类型和导入的嵌套命名空间具有相同的完全限定名称时，将发生此错误。 当引用该名称时，编译器不能区分这两者。 如果可以更改导入的源代码，则可以通过更改类型或命名空间的名称使这二者在程序集中唯一，从而解决该错误。  
  
 以下代码生成错误 CS0434。  
  
## 示例  
 此代码将创建该类型具有相同完全限定名称的第一个副本。  
  
```  
// CS0434_1.cs // compile with: /t:library namespace TypeBindConflicts { namespace NsImpAggPubImp { public class X { } } }  
```  
  
## 示例  
 此代码将创建该类型具有相同完全限定名称的第二个副本。  
  
```  
// CS0434_2.cs // compile with: /t:library namespace TypeBindConflicts { // Conflicts with another import (import2.cs). public class NsImpAggPubImp { } // Try this instead: // public class UniqueClassName { } }  
```  
  
## 示例  
 此代码将引用具有此相同完全限定名称的类型。  
  
```  
// CS0434.cs // compile with: /r:cs0434_1.dll /r:cs0434_2.dll using TypeBindConflicts; public class Test { public TypeBindConflicts.NsImpAggPubImp.X n2 = null; // CS0434 }  
```