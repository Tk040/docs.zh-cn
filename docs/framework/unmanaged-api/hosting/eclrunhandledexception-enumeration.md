---
description: 了解详细信息： EClrUnhandledException 枚举
title: EClrUnhandledException 枚举
ms.date: 03/30/2017
api_name:
- EClrUnhandledException
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EClrUnhandledException
helpviewer_keywords:
- EClrUnhandledException enumeration [.NET Framework hosting]
ms.assetid: d231044e-2b53-4836-93f9-8117ff0e5c3a
topic_type:
- apiref
ms.openlocfilehash: 088d448a92c4d9030208537b9c788477c85f9d37
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785544"
---
# <a name="eclrunhandledexception-enumeration"></a>EClrUnhandledException 枚举

介绍用于管理用户代码中未经处理的异常的可用选项。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum {  
    eRuntimeDeterminedPolicy,  
    eHostDeterminedPolicy  
} EClrUnhandledException;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`eRuntimeDeterminedPolicy`|指定发生默认行为。 进程已被破坏。|  
|`eHostDeterminedPolicy`|指定公共语言运行时 (CLR) 忽略未经处理的异常，并允许主机确定任何其他操作。|  
  
## <a name="remarks"></a>备注  

 若要指定 CLR 的行为类似于早期版本，请使用 `eHostDeterminedPolicy` 成员。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [EClrFailure 枚举](eclrfailure-enumeration.md)
- [EClrOperation 枚举](eclroperation-enumeration.md)
- [ICLRPolicyManager 接口](iclrpolicymanager-interface.md)
- [SetUnhandledExceptionPolicy 方法](iclrpolicymanager-setunhandledexceptionpolicy-method.md)
- [IHostPolicyManager 接口](ihostpolicymanager-interface.md)
- [承载枚举](hosting-enumerations.md)
