---
title: "泛型参数约束类型 &lt;typename&gt; 不符合 CLS | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc40040"
  - "vbc40040"
helpviewer_keywords: 
  - "BC40040"
ms.assetid: c640dd59-56a9-43ed-b199-32a60f7b9b06
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 泛型参数约束类型 &lt;typename&gt; 不符合 CLS
泛型类型标记为 `<CLSCompliant(True)>`但其类型形参之一的约束指定一个标记为 `<CLSCompliant(False)>` 的类型，没有标记或不合格的类型，因为它是不符合要求的类型。  
  
 对于符合 [语言独立性和与语言无关的组件](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md) \(CLS\) 的类型，必须只使用符合 CLS 的类型。 这还适用于对泛型类型的类型形参的约束。  
  
 以下 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 数据类型不符合 CLS：  
  
-   [SByte 数据类型](/dotnet/visual-basic/language-reference/data-types/sbyte-data-type)  
  
-   [UInteger 数据类型](/dotnet/visual-basic/language-reference/data-types/uinteger-data-type)  
  
-   [Ulong 数据类型](/dotnet/visual-basic/language-reference/data-types/ulong-data-type)  
  
-   [Ushort 数据类型](/dotnet/visual-basic/language-reference/data-types/ushort-data-type)  
  
 当将 <xref:System.CLSCompliantAttribute> 特性应用到编程元素中时，需要将该特性的 `isCompliant` 参数设置为 `True` 或 `False` 来指示符合或不符合性。 此参数没有默认值，必须为其提供一个值。  
  
 如果不将 <xref:System.CLSCompliantAttribute> 应用到元素，则它将被视为不符合规范。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的信息，请参见 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID:** BC40040  
  
### 更正此错误  
  
-   如果泛型类型必须获取这种特定类型约束的类型形参，请删除 <xref:System.CLSCompliantAttribute>。 类型不符合 CLS。  
  
-   如果泛型类型必须符合 CLS，则将此约束的类型改为最接近的符合 CLS 的类型。 例如，如果不需要 2147483647 以上的数值范围，可以使用 `Integer` 取代 `UInteger`。 如果确实需要更大范围，可以用 `Long` 代替 `UInteger`。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [\<PAVE OVER\>编写符合 CLS 的代码](http://msdn.microsoft.com/zh-cn/4c705105-69a2-4e5e-b24e-0633bc32c7f3)