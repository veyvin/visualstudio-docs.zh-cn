---
title: "枚举器 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: source control plug-ins, enumerators
ms.assetid: a60030c5-e1d1-47e1-84bb-cbfe838ab479
caps.latest.revision: "19"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.workload: vssdk
ms.openlocfilehash: 7929ead4ced01561adb8c11dcaa56bc97f57884b
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="enumerators"></a>枚举器
本部分列出了源代码管理插件必须要知道源控制插件 API 中的枚举器数据类型。  
  
## <a name="in-this-section"></a>本节内容  
 [命令代码](../extensibility/command-code-enumerator.md)  
 枚举的选项[SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md)和[SccPopulateList](../extensibility/sccpopulatelist-function.md)函数。  
  
 [消息](../extensibility/message-enumerator.md)  
 枚举标记用于打印的回调， [LPTEXTOUTPROC](../extensibility/lptextoutproc.md)。  
  
 [文件状态代码](../extensibility/file-status-code-enumerator.md)  
 包含指定的文件受源代码管理状态的命名常量值。  
  
 [目录状态代码](../extensibility/directory-status-code-enumerator.md)  
 包含指定的源控件下的目录状态的命名常量值。  
  
## <a name="related-sections"></a>相关章节  
 [创建源代码管理插件](../extensibility/internals/creating-a-source-control-plug-in.md)  
 定义源控件插件 SDK 并描述包含的资源。  
  
 [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md)  
 提示用户提供对于给定的命令的高级选项。  
  
 [SccPopulateList](../extensibility/sccpopulatelist-function.md)  
 检查以了解其当前状态的文件的列表。 此外，使用`pfnPopulate`函数以在文件不匹配的条件时通知调用方`nCommand`。  
  
 [LPTEXTOUTPROC](../extensibility/lptextoutproc.md)  
 描述由回调函数[SccOpenProject](../extensibility/sccopenproject-function.md)来从源代码管理插件通过 IDE 显示消息。  
  
 [源代码管理插件](../extensibility/source-control-plug-ins.md)  
 提供源控制插件 API 中的所有元素的完整的列表。