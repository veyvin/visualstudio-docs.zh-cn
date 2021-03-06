---
title: "编译器错误 CS0136 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0136"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0136"
ms.assetid: 379a1a7d-c52c-4f2b-9e77-c1107d26faf4
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0136
不能在此范围内声明名为“var”的局部变量，因为这样会使“var”具有不同的含义，而它已在 "parent or current\/child" 范围中表示其他内容了  
  
 变量声明隐藏了本应在范围内的另一个声明。 请重命名在生成 CS0136 的行上声明的变量。  
  
## 示例  
 下面的示例生成 CS0136：  
  
```  
// CS0136.cs  
namespace MyNamespace  
{  
   public class MyClass  
   {  
      public static void Main()  
      {  
         int i = 0;  
         {  
            char i = 'a';   // CS0136, hides int i  
         }  
         i++;  
      }  
   }  
}  
```  
  
 来自第 7.5.2.1 节中的 [C\# 语言规范](/dotnet/csharp/language-reference/language-specification)：  
  
 对于表达式或声明符中以简单名称形式给定的标识符的每个匹配项，直接封闭局部变量声明空间 \(§3.3\) 内的表达式或声明符中与简单名称相同的标识符的其他每个匹配项都必须引用同一个实体。 此规则可确保名称的含义在给定的块、switch 块、for\-、foreach\- 或 using\- 语句或匿名函数中始终相同。