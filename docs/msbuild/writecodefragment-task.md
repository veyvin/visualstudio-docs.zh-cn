---
title: "WriteCodeFragment 任务 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, WriteCodeFragment task
- WriteCodeFragment task [MSBuild]
ms.assetid: 1d2514b4-5bef-43bb-bebe-496da8ef063c
caps.latest.revision: "5"
author: kempb
ms.author: kempb
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: d4a781526b64305225325f34c5407ff68afa13c8
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="writecodefragment-task"></a>WriteCodeFragment 任务
根据指定的生成代码片段，生成临时代码文件。 不会删除该文件。  
  
## <a name="parameters"></a>参数  
 下表描述了 `WriteCodeFragment` 任务的参数。  
  
|参数|描述|  
|---------------|-----------------|  
|`AssemblyAttributes`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 要编写的属性的说明。 项目 `Include` 值是属性的完整类型名称，例如“System.AssemblyVersionAttribute”。<br /><br /> 每个元数据都是参数的名称/值对，必须为类型 `String`。 某些属性只允许使用位置构造函数参数。 但可在任何属性中使用这些参数。 若要设置位置构造函数属性，请使用类似于“_Parameter1”、“_Parameter2”等元数据名称。<br /><br /> 不能跳过参数索引。|  
|`Language`|必选 `String` 参数。<br /><br /> 指定要生成的代码的语言。<br /><br /> `Language` 可以是任何可用于 CodeDom 提供程序的语言，例如“C#”或“VisualBasic”。 发出的文件将具有该语言的默认文件扩展名。|  
|`OutputDirectory`|可选 <xref:Microsoft.Build.Framework.ITaskItem> 参数。<br /><br /> 指定生成代码的目标文件夹，通常为中间文件夹。|  
|`OutputFile`|可选 <xref:Microsoft.Build.Framework.ITaskItem> 输出参数。<br /><br /> 指定已生成文件的路径。 如果使用文件名设置此参数，则会将目标文件夹附加在文件名前。 如果使用根设置，则会忽略目标文件夹。<br /><br /> 如果未设置此参数，输出文件名将为目标文件夹、任意文件名称和指定语言的默认文件扩展名。|  
  
## <a name="remarks"></a>备注  
 除了具有表中列出的参数外，此任务还将从本身继承自 <xref:Microsoft.Build.Utilities.Task> 类的 <xref:Microsoft.Build.Tasks.TaskExtension> 类继承参数。 有关这些其他参数的列表及其说明的信息，请参阅 [TaskExtension Base Class](../msbuild/taskextension-base-class.md)。  
  
## <a name="see-also"></a>请参阅  
 [任务](../msbuild/msbuild-tasks.md)   
 [任务参考](../msbuild/msbuild-task-reference.md)