---
title: "特性构造函数具有“&lt;type&gt;”类型的参数，此参数不是整型、浮点型或枚举类型，也不是 Char、String、Boolean、System.Type 之一或这些类型的一维数组 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30045"
  - "vbc30045"
helpviewer_keywords: 
  - "BC30045"
ms.assetid: 16899755-7901-4c56-ae90-54c3532e8319
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 特性构造函数具有“&lt;type&gt;”类型的参数，此参数不是整型、浮点型或枚举类型，也不是 Char、String、Boolean、System.Type 之一或这些类型的一维数组
自定义特性定义包括对参数指定无效数据类型的构造函数。 特性只能以某些数据类型作为参数，因为只有这些类型可序列化到程序集的元数据。  
  
 **错误 ID：**BC30045  
  
### 更正此错误  
  
1.  将参数的数据类型更改为 `Byte`、`Short`、`Integer`、`Long`、`Single`、`Double`、`Char`、`String`、`Boolean`、`System.Type` 或枚举类型。  
  
## 请参阅  
 [不在生成中：Visual Basic 中的自定义特性](http://msdn.microsoft.com/zh-cn/d72d8a5c-8f64-4614-b15b-cad66845d047)