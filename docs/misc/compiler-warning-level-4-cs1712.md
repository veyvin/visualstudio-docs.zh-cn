---
title: "编译器警告（等级 4）CS1712 | Microsoft Docs"
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
  - "CS1712"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1712"
ms.assetid: d9a8be26-c0ba-41fa-b082-1ce4ba7724b7
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器警告（等级 4）CS1712
类型参数“type parameter”在“type”的 XML 注释中没有匹配的 typeparam 标记（但其他类型参数有）  
  
 泛型类型的文档缺少 **typeparam** 标记。 有关更多信息，请参见[\<typeparam\>](../Topic/%3Ctypeparam%3E%20\(C%23%20Programming%20Guide\).md)。  
  
## 示例  
 下面的代码生成 CS1712。 若要解决此错误，请为类型参数 S 添加 **typeparam** 标记。  
  
```  
// CS1712.cs // compile with: /doc:cs1712.xml using System; class Test { public static void Main() {} /// <param name="j"> This is the j parameter.</param> /// <typeparam name="T"> This is the T type parameter.</typeparam> public void bar<T,S>(int j) {}  // CS1712 }  
```