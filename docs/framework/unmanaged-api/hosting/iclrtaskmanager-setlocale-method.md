---
description: 了解详细信息： ICLRTaskManager：： SetLocale 方法
title: ICLRTaskManager::SetLocale 方法
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.SetLocale
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::SetLocale
helpviewer_keywords:
- SetLocale method, ICLRTaskManager interface [.NET Framework hosting]
- ICLRTaskManager::SetLocale method [.NET Framework hosting]
ms.assetid: ed16bb7f-4206-43a8-b9e9-c5737b69e3af
topic_type:
- apiref
ms.openlocfilehash: 401f227f900ab4b89cd6fc5b7902b4314a7687e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799468"
---
# <a name="iclrtaskmanagersetlocale-method"></a>ICLRTaskManager::SetLocale 方法

通知公共语言运行时 (CLR) 宿主已修改区域设置标识符的值 (该标识符映射到当前正在执行的任务) 的地理区域和语言。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT SetLocale (  
    [in] LCID lcid  
);  
```  
  
## <a name="parameters"></a>参数  

 `lcid`  
 中映射到新分配的地理区域和语言的区域设置标识符值。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|S_OK|该方法已成功返回。|  
|HOST_E_CLRNOTAVAILABLE|CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。|  
|HOST_E_TIMEOUT|调用超时。|  
|HOST_E_NOT_OWNER|调用方不拥有该锁。|  
|HOST_E_ABANDONED|已阻止的线程或纤程正在等待某个事件时，该事件被取消。|  
|E_FAIL|发生未知的灾难性故障。 当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。 对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。|  
  
## <a name="remarks"></a>备注  

 `SetLocale` 使宿主有机会执行它可能对区域设置进行同步的任何机制。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRTask 接口](iclrtask-interface.md)
- [ICLRTaskManager 接口](iclrtaskmanager-interface.md)
- [IHostTask 接口](ihosttask-interface.md)
- [IHostTaskManager 接口](ihosttaskmanager-interface.md)
