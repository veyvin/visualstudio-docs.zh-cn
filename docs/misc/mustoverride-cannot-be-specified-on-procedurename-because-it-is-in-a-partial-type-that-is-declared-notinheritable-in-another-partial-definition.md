---
title: "不能在“&lt;procedurename&gt;”上指定“MustOverride”，因为它所在的分部类型在另一个分部定义中被声明为“NotInheritable” | Microsoft Docs"
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
  - "vbc30927"
  - "BC30927"
helpviewer_keywords: 
  - "BC30927"
ms.assetid: 5798dfda-3d7b-4f30-9715-40cbf52d6dc4
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 不能在“&lt;procedurename&gt;”上指定“MustOverride”，因为它所在的分部类型在另一个分部定义中被声明为“NotInheritable”
在类中将过程或属性声明为 `MustOverride`，该类在多个分部声明中定义，但其中一个分部定义为该类指定了 `NotInheritable`。  
  
 在多个分部声明间划分类的定义时，编译器会将该类视为它的所有分部声明的联合。 这不仅适用于成员，还适用于实现、继承和访问级别。  
  
 若要重写过程或属性，类必须从基类继承它。 因此，若要在基类中为过程或属性指定 `MustOverride`，必须为类指定 `MustInherit`。 不能为同一个类同时指定 `MustInherit` 和 `NotInheritable`，因为它们互相矛盾。  
  
 **错误 ID：**BC30927  
  
### 更正此错误  
  
-   如果必须重写的属性或过程，则从 `NotInheritable` 关键字出现的分部声明中将其删除。  
  
-   如果类必须为 `NotInheritable`，则从过程或属性中删除 `MustOverride` 关键字。 因为不能继承此类，所以不能重写它。  
  
## 请参阅  
 [分部](/dotnet/visual-basic/language-reference/modifiers/partial)   
 [MustOverride](/dotnet/visual-basic/language-reference/modifiers/mustoverride)   
 [MustInherit](/dotnet/visual-basic/language-reference/modifiers/mustinherit)   
 [NotInheritable](/dotnet/visual-basic/language-reference/modifiers/notinheritable)   
 [继承的基础知识](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)