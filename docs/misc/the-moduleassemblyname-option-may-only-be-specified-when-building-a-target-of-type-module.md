---
title: "只有在生成“module”类型的目标时才能指定 /moduleassemblyname 选项 | Microsoft Docs"
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
  - "bc2030"
  - "vbc2030"
helpviewer_keywords: 
  - "BC2030"
ms.assetid: 2ebc577b-3464-40cc-8788-9fc9d3b4f928
caps.latest.revision: 3
caps.handback.revision: 3
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 只有在生成“module”类型的目标时才能指定 /moduleassemblyname 选项
当将 `/target` 选项设置为 `module` 之外的值时，已向 Visual Basic 编译器传递 `/moduleassemblyname` 编译器选项。  
  
 **错误 ID：** BC2030  
  
### 更正此错误  
  
1.  删除 `/moduleassemblyname` 编译器选项或将 `/target` 选项设置为 `module`。  
  
## 请参阅  
 [\/target](/dotnet/visual-basic/reference/command-line-compiler/target)   
 [\/moduleassemblyname](/dotnet/visual-basic/reference/command-line-compiler/moduleassemblyname)   
 [Visual Basic 命令行编译器](/dotnet/visual-basic/reference/command-line-compiler/index)