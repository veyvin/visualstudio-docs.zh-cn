---
title: "生成程序集时检测到可能存在的问题：&lt;error&gt; | Microsoft Docs"
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
  - "vbc40009"
  - "bc40009"
helpviewer_keywords: 
  - "BC40009"
ms.assetid: 4bc5108a-a96e-43be-8bba-a47441a25f3e
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 生成程序集时检测到可能存在的问题：&lt;error&gt;
由 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 编译器调用的 ALink 工具报告生成程序集时发生的错误。 可能原因之一是已签名的程序集引用未签名的程序集。  
  
 此消息是一个警告。 编译器将继续生成程序集。 有关隐藏警告或将警告视为错误的详细信息，请参阅[在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC40009  
  
### 更正此错误  
  
1.  检查引用的错误信息并采取相应的操作。  
  
2.  再次编译此程序以查看错误是否重复出现。  
  
3.  如果错误重复出现，请重新安装 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 编译器。  
  
4.  如果重新安装后仍然出现错误，请收集有关该情况的信息并通知 Microsoft 产品支持服务。  
  
## 请参阅  
 [PAVEOVER 产品支持和辅助功能](http://msdn.microsoft.com/zh-cn/14e1d293-7b6d-40a6-bf3e-a92f8ee6c88c)