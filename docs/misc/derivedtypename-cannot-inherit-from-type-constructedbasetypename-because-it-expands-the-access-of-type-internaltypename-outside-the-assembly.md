---
title: "“&lt;derivedtypename&gt;”无法从 &lt;type&gt;“&lt;constructedbasetypename&gt;”继承，因为它会将类型“&lt;internaltypename&gt;”的访问扩展到程序集外部 | Microsoft Docs"
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
  - "BC30922"
  - "vbc30922"
helpviewer_keywords: 
  - "BC30922"
ms.assetid: 81909654-7e67-4b89-81a3-25ae57f678f7
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;derivedtypename&gt;”无法从 &lt;type&gt;“&lt;constructedbasetypename&gt;”继承，因为它会将类型“&lt;internaltypename&gt;”的访问扩展到程序集外部
派生的类或接口尝试通过将受限类型作为基类或接口的类型参数来扩展其访问级别。  
  
 以下代码会生成此错误。  
  
```  
Public Class baseClass(Of t)  
End Class  
Public Class derivedClass  
    Inherits baseClass(Of restrictedStructure)  
End Class  
Friend Structure restrictedStructure  
    Dim firstMember As Integer  
End Structure  
```  
  
 不允许程序集外部的代码访问 `restrictedStructure`。 但是，`derivedClass` 可以从可引用它的任何代码进行访问。 因此，如果 `derivedClass` 使用 `restrictedStructure` 作类型参数，它将不能继承 `baseClass`，因为这样会向任何程序集中的代码公开 `restrictedStructure`。  
  
 **错误 ID：**BC30922  
  
### 更正此错误  
  
-   调整类或接口的访问级别，以便派生的类型不会扩展受限制类型的访问级别。  
  
     \- 或 \-  
  
-   如果不能调整访问级别，请勿在构造基类或接口时将受限类型用作类型参数。  
  
## 请参阅  
 [Inherits 语句](/dotnet/visual-basic/language-reference/statements/inherits-statement)   
 [继承的基础知识](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)   
 [Visual Basic 中的访问级别](/dotnet/visual-basic/programming-guide/language-features/declared-elements/access-levels)   
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [类型列表](/dotnet/visual-basic/language-reference/statements/type-list)