---
title: "Idiastackframe:: Get_rawlvarinstancevalue |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaStackFrame::get_rawLVarInstanceValue method
ms.assetid: ce526259-85a6-475b-9274-0b3a21d95db2
caps.latest.revision: "10"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 5872c77a9154c72f6c3bcd76452792cff34452cb
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="idiastackframegetrawlvarinstancevalue"></a>IDiaStackFrame::get_rawLVarInstanceValue
此方法以原始字节形式检索指定的本地变量的值。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT get_rawLVarInstanceValue(  
   IDiaLVarInstance* pInstance,  
   DWORD             cbDataMax,  
   DWORD*            pcbData,  
   BYTE*             pbData  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pInstance`  
 [in]`IDiaLVarInstance`对象表示要获取的值的本地变量的实例。  
  
 `cbDataMax`  
 [in]最大缓冲区中的字节数指向的`pbData`。 这可能是最多 8 个字节 (`sizeof(ULONGLONG)`)。  
  
 `pcbData`  
 [out]返回的实际存储在缓冲区中的字节数。  
  
 `pbData`  
 [out]若要使用数据填充缓冲区。 这不能为`NULL`。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="see-also"></a>请参阅  
 [IDiaStackFrame](../../debugger/debug-interface-access/idiastackframe.md)