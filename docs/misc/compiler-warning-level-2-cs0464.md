---
title: "编译器警告（等级 2）CS0464 | Microsoft Docs"
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
  - "CS0464"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0464"
ms.assetid: 3dff97d4-e1f6-4a71-91e2-68cffc38d49a
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器警告（等级 2）CS0464
与“type”类型的 null 进行比较始终产生“false”  
  
 当你在可以为 null 的变量与 null 之间进行比较时，如果比较不为 `==` 或 `!=`，将出现此警告。 若要解决此错误，请验证你是否确实要检查值是否为 `null`。 类似 `i == null` 这样的比较结果既可以为 true，也可以为 false。 类似 `i > null` 这样的比较结果始终为 false。  
  
## 示例  
 下面的示例生成 CS0464。  
  
```  
// CS0464.cs class MyClass { public static void Main() { int? i = 0; if (i < null) ;   // CS0464 i++; } }  
```