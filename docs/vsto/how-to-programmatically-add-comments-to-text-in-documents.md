---
title: "如何： 以编程方式向文档中的文本添加注释 |Microsoft 文档"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- comments, adding to documents
- documents [Office development in Visual Studio], adding comments
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.workload: office
ms.openlocfilehash: 2702d8aed4dce16a2dde1c42b2b1410ebded14e3
ms.sourcegitcommit: f9fbf1f55f9ac14e4e5c6ae58c30dc1800ca6cda
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/10/2018
---
# <a name="how-to-programmatically-add-comments-to-text-in-documents"></a>如何：以编程方式向文档中的文本添加注释
  文档类的注释属性将添加到的 Microsoft Office Word 文档中的文本范围的注释。  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
 下列示例将在文档中的第一个段落添加注释。  
  
### <a name="to-add-a-new-comment-to-text-in-a-document-level-customization"></a>向文档级自定义项中的文本添加新注释  
  
1.  调用 <xref:Microsoft.Office.Interop.Word.Comments.Add%2A> 属性的 <xref:Microsoft.Office.Tools.Word.Document.Comments%2A> 方法并提供范围和注释文本。 若要使用下面的代码示例，请从项目的 `ThisDocument` 类中运行它。  
  
     [!code-vb[Trin_VstcoreWordAutomation#118](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#118)]
     [!code-csharp[Trin_VstcoreWordAutomation#118](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#118)]  
  
### <a name="to-add-a-new-comment-to-text-in-an-vsto-add-in"></a>向 VSTO 外接程序中的文本添加新注释  
  
1.  调用 <xref:Microsoft.Office.Interop.Word.Comments.Add%2A> 属性的 <xref:Microsoft.Office.Interop.Word._Document.Comments%2A> 方法并提供范围和注释文本。  
  
     下面的代码示例将向活动文档中添加注释。 若要使用此示例，请从项目的 `ThisAddIn` 类中运行它。  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#118](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#118)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#118](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#118)]  
  
## <a name="robust-programming"></a>可靠编程  
 若要更改 Word 在注释中添加的用户缩写，请使用 <xref:Microsoft.Office.Interop.Word._Application.UserInitials%2A> 属性。  
  
## <a name="see-also"></a>请参阅  
 [如何： 以编程方式移除文档中所有注释](../vsto/how-to-programmatically-remove-all-comments-from-documents.md)   
 [文档主机项](../vsto/document-host-item.md)  
  
  