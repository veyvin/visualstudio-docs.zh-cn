---
title: "join 方法 (Array) (JavaScript) |Microsoft 文档"
ms.custom: 
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: 
ms.suite: 
ms.technology: devlang-javascript
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: join
dev_langs:
- JavaScript
- TypeScript
- DHTML
helpviewer_keywords:
- Join method
- concatenating strings, join method
- arrays [Visual Studio], joining
ms.assetid: 20f8fde1-014b-488e-9008-464a86e6b21f
caps.latest.revision: "16"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4591b12b3556384fef3e367d20cf9545d2f3dedd
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/27/2017
---
# <a name="join-method-array-javascript"></a>join 方法 (Array) (JavaScript)
将添加数组由指定的分隔符字符串分隔的所有的元素。  
  
## <a name="syntax"></a>语法  
  
```  
  
arrayObj.join([separator])   
```  
  
## <a name="parameters"></a>参数  
 `arrayObj`  
 必需。 一个 `Array` 对象。  
  
 `separator`  
 可选。 用于与在随后出现下分开数组的一个元素的字符串`String`。 如果省略，用逗号分隔数组元素。  
  
## <a name="remarks"></a>备注  
 如果数组的任何元素**未定义**或`null`，它将被视为空字符串。  
  
## <a name="example"></a>示例  
 下面的示例演示如何使用**联接**方法。  
  
```JavaScript  
var a, b;  
a = new Array(0,1,2,3,4);  
b = a.join("-");  
document.write(b);  
  
// Output:  
// 0-1-2-3-4  
  
```  
  
## <a name="requirements"></a>要求  
 [!INCLUDE[jsv2](../../javascript/reference/includes/jsv2-md.md)]  
  
## <a name="see-also"></a>另请参阅  
 [String 对象](../../javascript/reference/string-object-javascript.md)