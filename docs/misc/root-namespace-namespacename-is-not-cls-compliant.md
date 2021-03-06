---
title: "根命名空间 &lt;命名空间&gt; 不符合 CLS | Microsoft Docs"
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
  - "bc40038"
  - "vbc40038"
helpviewer_keywords: 
  - "BC40038"
ms.assetid: ec850295-b2fe-4f19-b808-d22fe0aaa32d
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 根命名空间 &lt;命名空间&gt; 不符合 CLS
程序集标记为 `<CLSCompliant(True)>`，但根命名空间名称以下划线 \(`_`\) 开头。  
  
 编程元素可以包含一个或多个下划线，但要符合 [语言独立性和与语言无关的组件](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md) \(CLS\)，且其不得以下划线开头。 请参阅 [已声明的元素名称](/dotnet/visual-basic/programming-guide/language-features/declared-elements/declared-element-names)。  
  
 当将 <xref:System.CLSCompliantAttribute> 应用到编程元素中时，需要将该特性的 `isCompliant` 参数设置为 `True` 或 `False` 来指示符合或不符合性。 此参数没有默认值，必须为其提供一个值。  
  
 如果不将 <xref:System.CLSCompliantAttribute> 应用到元素，则它将被视为不符合规范。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的信息，请参见 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC40038  
  
### 更正此错误  
  
-   如果你需要 CLS 遵从性，请更改根命名空间名称，使其不以下划线开头。  
  
-   如果你需要根命名空间名称保持不变，则从程序集删除 <xref:System.CLSCompliantAttribute> 或将其标记为 `<CLSCompliant(False)>`。  
  
## 请参阅  
 [Namespace 语句](/dotnet/visual-basic/language-reference/statements/namespace-statement)   
 [Visual Basic 中的命名空间](/dotnet/visual-basic/programming-guide/program-structure/namespaces)   
 [\/rootnamespace](/dotnet/visual-basic/reference/command-line-compiler/rootnamespace)   
 [NIB：如何：更改应用程序的命名空间 \(Visual Basic\)](http://msdn.microsoft.com/zh-cn/029d85c0-e173-4f7a-afba-a29f3aaf6ebf)   
 [已声明的元素名称](/dotnet/visual-basic/programming-guide/language-features/declared-elements/declared-element-names)   
 [Visual Basic 命名约定](/dotnet/visual-basic/programming-guide/program-structure/naming-conventions)   
 [\<PAVE OVER\>编写符合 CLS 的代码](http://msdn.microsoft.com/zh-cn/4c705105-69a2-4e5e-b24e-0633bc32c7f3)