---
title: "CA5351 不使用损坏的加密算法 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 483f51b3-e186-4433-b48e-5ca24a9a9c94
caps.latest.revision: "12"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: fd9959fe67097b815a4a86b81b5cf78e468281a5
ms.sourcegitcommit: 49aa031cbebdd9c7ec070c713afb1a97d1ecb701
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2018
---
# <a name="ca5351-do-not-use-broken-cryptographic-algorithms"></a>CA5351 不使用损坏的加密算法
|||  
|-|-|  
|TypeName|DoNotUseBrokenCryptographicAlgorithms|  
|CheckId|CA5351|  
|类别|Microsoft.Cryptography|  
|是否重大更改|非重大更改|  
  
> [!NOTE]
>  此警告上次更新于 2015 年 11 月。  
  
## <a name="cause"></a>原因  
 哈希函数（如 <xref:System.Security.Cryptography.MD5> ）和加密算法（如 <xref:System.Security.Cryptography.DES> 和 <xref:System.Security.Cryptography.RC2> ）可能会带来重大风险，并可能通过普通的攻击技术（如暴力攻击和哈希冲突）导致暴露敏感信息。  
  
 下面的加密算法列表受到已知加密攻击。 加密哈希算法 <xref:System.Security.Cryptography.MD5> 受到哈希冲突攻击。  根据使用情况，哈希冲突可能会使依赖哈希函数这一唯一加密输出的系统受到假冒、篡改或其他类型的攻击。 加密算法 <xref:System.Security.Cryptography.DES> 和 <xref:System.Security.Cryptography.RC2> 受到加密攻击，可能会导致加密数据的意外泄露。  
  
## <a name="rule-description"></a>规则说明  
 损坏的加密算法不安全，不鼓励继续使用。 尽管具体的漏洞因使用环境的不同而异，但 MD5 哈希算法仍易遭到已知的冲突攻击。  用于确保数据完整性的哈希算法（例如文件签名或数字证书）尤其易被攻击。  在这种情况下，攻击者可能会生成两个独立的数据块，以便在不更改哈希值或使相关数字签名无效的情况下，将良性数据替换为恶意数据。  
  
 对于加密算法：  
  
-   <xref:System.Security.Cryptography.DES> 加密使用的密钥强度较低，可能在一天内被暴力破解。  
  
-   <xref:System.Security.Cryptography.RC2> 加密容易遭受与密钥相关的攻击，攻击者可以通过这些攻击找出所有密钥值之间的数学关系。  
  
 当在源代码中找到上述任何加密函数时，将触发此规则并向用户发出警告。  
  
## <a name="how-to-fix-violations"></a>如何解决冲突  
 使用更强大的加密选项：  
  
-   对于 MD5，请使用中的哈希[sha-2](https://msdn.microsoft.com/library/windows/desktop/aa382459.aspx)系列 (例如<xref:System.Security.Cryptography.SHA512>， <xref:System.Security.Cryptography.SHA384>， <xref:System.Security.Cryptography.SHA256>)。  
  
-   对于 DES 和 RC2，请使用 <xref:System.Security.Cryptography.Aes> 加密。  
  
## <a name="when-to-suppress-warnings"></a>何时禁止显示警告  
 除非经过加密专家审查，否则不要禁止显示此规则的警告。  
  
## <a name="pseudo-code-example"></a>伪代码示例  
 下面的伪代码示例演示此规则检测到的模式和可能的替代模式。  
  
### <a name="md5-hashing-violation"></a>MD5 哈希冲突  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = MD5.Create();  
  
```  
  
### <a name="solution"></a>解决方案  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = SHA256.Create();  
  
```  
  
### <a name="rc2-encryption-violation"></a>RC2 加密冲突  
  
```  
using System.Security.Cryptography;   
...    
RC2 encAlg = RC2.Create();  
  
```  
  
### <a name="solution"></a>解决方案  
  
```  
using System.Security.Cryptography;   
...   
using (AesManaged encAlg = new AesManaged())   
{   
  ...   
}  
```  
  
### <a name="des-br-br-encryption-violation"></a>DES <br /><br />加密冲突  
  
```  
using System.Security.Cryptography;   
...   
DES encAlg = DES.Create();  
  
```  
  
### <a name="solution"></a>解决方案  
  
```  
using System.Security.Cryptography;   
...   
using (AesManaged encAlg = new AesManaged())   
{   
  ...   
}  
```