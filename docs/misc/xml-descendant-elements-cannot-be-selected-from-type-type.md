---
title: "XML 子代元素不能从类型“type”中选择 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc36809"
  - "bc36809"
helpviewer_keywords: 
  - "BC36809"
ms.assetid: 560a3370-f24d-4ca3-93b1-39aabe13c238
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# XML 子代元素不能从类型“type”中选择
已针对不属于类型 <xref:System.Xml.Linq.XElement>、<xref:System.Xml.Linq.XDocument> 或 `IEnumerable(Of XElement)` 的对象引用一个 XML 子代。 有关更多信息，请参见[XML 后代轴属性](/dotnet/visual-basic/language-reference/xml-axis/xml-descendant-axis-property)。  
  
```vb#  
' Generates an error. Dim var = "sample text"...<childElement>  
```  
  
 **错误 ID：**BC36809  
  
### 更正此错误  
  
-   确保正在引用其子代元素的对象被强类型化为 <xref:System.Xml.Linq.XElement>、<xref:System.Xml.Linq.XDocument> 或 `IEnumerable(Of XElement)`。 下面是一个示例：  
  
    ```vb#  
    Dim elem As XElement = <root> <child /> </root> Dim var = elem...<child>  
    ```  
  
## 请参阅  
 [XML 后代轴属性](/dotnet/visual-basic/language-reference/xml-axis/xml-descendant-axis-property)   
 [XML 轴属性](/dotnet/visual-basic/language-reference/xml-axis/xml-axis-properties)   
 [XML](/dotnet/visual-basic/programming-guide/language-features/xml/index)