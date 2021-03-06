---
description: 了解详细信息： IMetaDataEmit：： SetTypeDefProps 方法
title: IMetaDataEmit::SetTypeDefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetTypeDefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetTypeDefProps
helpviewer_keywords:
- SetTypeDefProps method [.NET Framework metadata]
- IMetaDataEmit::SetTypeDefProps method [.NET Framework metadata]
ms.assetid: 480d596a-759f-4d29-ac1a-3dbff8f3544d
topic_type:
- apiref
ms.openlocfilehash: 1160d20e7ceb422390f8cd725a75fdb4f42318e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706495"
---
# <a name="imetadataemitsettypedefprops-method"></a>IMetaDataEmit::SetTypeDefProps 方法

设置由之前调用 [IMetaDataEmit：:D efinetypedef](imetadataemit-definetypedef-method.md)定义的类型的功能。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT SetTypeDefProps (  
    [in]  mdTypeDef   td,
    [in]  DWORD       dwTypeDefFlags,
    [in]  mdToken     tkExtends,
    [in]  mdToken     rtkImplements[]
);  
```  
  
## <a name="parameters"></a>参数  

 `td`  
 中 `mdTypeDef` 从对 IMetaDataEmit 的原始调用获取的标记 [：:D efinetypedef](imetadataemit-definetypedef-method.md)。  
  
 `dwTypeDefFlags`  
 [in] `TypeDef` 属性. 这是一个值的位掩码 `CorTypeAttr` 。  
  
 `tkExtends`  
 中 `mdToken` 基类的。 从之前对 IMetaDataEmit 的调用中获取 [：:D efineimporttype](imetadataemit-defineimporttype-method.md)或 `null` 。  
  
 `rtkImplements[]`  
 中此类型实现的接口的标记数组。 `mdTypeRef`使用[IMetaDataEmit：:D efineimporttype](imetadataemit-defineimporttype-method.md)获取这些令牌。 数组的最后一个元素必须是 `mdTokenNil` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MSCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataEmit 接口](imetadataemit-interface.md)
- [IMetaDataEmit2 接口](imetadataemit2-interface.md)
