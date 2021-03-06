---
description: 了解详细信息： ICorDebugHeapValue2：： CreateHandle 方法
title: ICorDebugHeapValue2::CreateHandle 方法
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue2.CreateHandle
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue2::CreateHandle
helpviewer_keywords:
- CreateHandle method [.NET Framework debugging]
- ICorDebugHeapValue2::CreateHandle method [.NET Framework debugging]
ms.assetid: fbc418e8-fa22-420d-84ec-e0e1800db041
topic_type:
- apiref
ms.openlocfilehash: d93fee71441b9c510d517acb9582b8d1d9ce9e10
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803654"
---
# <a name="icordebugheapvalue2createhandle-method"></a>ICorDebugHeapValue2::CreateHandle 方法

为此 ICorDebugHeapValue2 对象表示的堆值创建指定类型的句柄。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateHandle (  
    [in] CorDebugHandleType      type,
    [out] ICorDebugHandleValue   **ppHandle  
);  
```  
  
## <a name="parameters"></a>参数  

 `type`  
 中CorDebugHandleType 枚举的一个值，该值指定要创建的句柄的类型。  
  
 `ppHandle`  
 弄指向 ICorDebugHandleValue 对象的地址的指针，该对象表示此堆值的新句柄。  
  
## <a name="remarks"></a>备注  

 该句柄将在与堆值相关联的应用程序域中创建，如果应用程序域已卸载，则将变为无效。  
  
 对于同一堆值多次调用此函数会创建多个句柄。 因为句柄会影响垃圾回收器的性能，所以调试程序应将自身限制为相对较少数量的句柄， (每次处于活动状态的 256) 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
