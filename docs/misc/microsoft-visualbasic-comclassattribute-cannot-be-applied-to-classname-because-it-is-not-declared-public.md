---
title: "“Microsoft.VisualBasic.ComClassAttribute”不能应用于“&lt;classname&gt;”，因为它未声明为“Public” | Microsoft Docs"
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
  - "bc32509"
  - "vbc32509"
helpviewer_keywords: 
  - "BC32509"
ms.assetid: ac46851f-53ab-4ce6-87b1-4c4d29508527
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “Microsoft.VisualBasic.ComClassAttribute”不能应用于“&lt;classname&gt;”，因为它未声明为“Public”
类是用 <xref:Microsoft.VisualBasic.ComClassAttribute> 进行声明的，但其声明未指定 `Public`。  
  
 .NET Framework 类必须满足以下要求，才可进行 COM 互操作：  
  
-   它必须为 `Public`，其所有容器必须为 `Public`，且它必须至少公开一个 `Public` 成员。  
  
-   它不能为*抽象*，即它不能用 `MustInherit` 进行声明。  
  
-   它不能为泛型，也不能在泛型容器类型中进行声明。  
  
 **错误 ID：**BC32509  
  
### 更正此错误  
  
-   将 `Public` 关键字添加到类声明。  
  
     \- 或 \-  
  
-   如果类或其包含元素不能为 `Public`，则请从类声明中删除 <xref:Microsoft.VisualBasic.ComClassAttribute>。 不能将其公开给 COM。  
  
## 请参阅  
 <xref:Microsoft.VisualBasic.ComClassAttribute>   
 [COM 互操作](/dotnet/visual-basic/programming-guide/com-interop/index)   
 [Public](/dotnet/visual-basic/language-reference/modifiers/public)