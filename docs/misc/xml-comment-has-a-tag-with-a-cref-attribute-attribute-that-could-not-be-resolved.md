---
title: "XML 注释中的一个标记具有未能解析的“cref”特性“&lt;attribute&gt;” | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc42309"
  - "vbc42309"
helpviewer_keywords: 
  - "BC42309"
ms.assetid: c9f3cfa5-565f-48bf-8616-cfb25d24f89e
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# XML 注释中的一个标记具有未能解析的“cref”特性“&lt;attribute&gt;”
XML 注释中的一个标记具有未能解析的“cref”特性 \<attribute\>。 将忽略 XML 注释。  
  
 标记的一个 `cref` 特性可能通过指定标识符的相对名称指定了指向 XML 的另一个元素的链接。 在编译时，编译器会将值替换为用户指向的值的限定 XML 标识符。 编译器会使用其正常解析规则查找类型或成员。  
  
 **错误 ID：**BC42309  
  
### 更正此错误  
  
-   验证 `cref` 特性，使它指向有效的代码元素。  
  
## 请参阅  
 [如何：创建 XML 文档](../Topic/How%20to:%20Create%20XML%20Documentation%20in%20Visual%20Basic.md)   
 [XML 注释标记](/dotnet/visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments)