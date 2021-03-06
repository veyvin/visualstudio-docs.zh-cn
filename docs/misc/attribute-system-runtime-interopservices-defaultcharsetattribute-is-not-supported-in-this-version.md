---
title: "此版本不支持特性“System.Runtime.InteropServices.DefaultCharSetAttribute” | Microsoft Docs"
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
  - "bc32510"
  - "vbc32510"
helpviewer_keywords: 
  - "BC32510"
ms.assetid: e2eec233-6e0b-4f2f-a801-b0274e579c0e
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 此版本不支持特性“System.Runtime.InteropServices.DefaultCharSetAttribute”
可通过 <xref:System.Runtime.InteropServices.DefaultCharSetAttribute?displayProperty=fullName> 特性指定要在封送的字符串中使用的字符集。 其值接受 <xref:System.Runtime.InteropServices.CharSet?displayProperty=fullName> 枚举的成员。  
  
 当前版本的 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 不支持此特性。 未来版本中可能提供支持。  
  
 **错误 ID：**BC32510  
  
### 更正此错误  
  
-   使用每个 [Declare 语句](/dotnet/visual-basic/language-reference/statements/declare-statement) 为其声明的外部过程指定字符集。 下面的示例阐释了这一点。  
  
    ```  
    Ansi Declare Function GetUserName Lib "advapi32.dll" _ (ByVal lpBuffer As String, ByRef nSize As Integer) As Integer Unicode Declare Sub externalProc Lib "projectlib.dll" _ (ByVal arg As Double)  
    ```  
  
     如果在 `Declare` 语句中不指定字符集，则默认为 ANSI。  
  
## 请参阅  
 <xref:System.Runtime.InteropServices.DefaultCharSetAttribute>   
 <xref:System.Runtime.InteropServices.CharSet>   
 [不在生成中：Visual Basic 中的特性](http://msdn.microsoft.com/zh-cn/620bfc0e-4582-4c8b-8432-ebc5c3dccc22)   
 [Declare 语句](/dotnet/visual-basic/language-reference/statements/declare-statement)