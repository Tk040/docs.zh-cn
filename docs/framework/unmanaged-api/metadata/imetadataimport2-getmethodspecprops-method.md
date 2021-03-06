---
description: 了解详细信息： IMetaDataImport2：： GetMethodSpecProps 方法
title: IMetaDataImport2::GetMethodSpecProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetMethodSpecProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetMethodSpecProps
helpviewer_keywords:
- GetMethodSpecProps method [.NET Framework metadata]
- IMetaDataImport2::GetMethodSpecProps method [.NET Framework metadata]
ms.assetid: 9544b711-e669-4eaf-8630-ee862e5e4489
topic_type:
- apiref
ms.openlocfilehash: 77f3f78905d1f7f44af0e9c7a75746b4e5b6e684
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688645"
---
# <a name="imetadataimport2getmethodspecprops-method"></a>IMetaDataImport2::GetMethodSpecProps 方法

获取指定的 MethodSpec 标记所引用的方法的元数据签名。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetMethodSpecProps (  
   [in]  mdMethodSpec     mi,  
   [out] mdToken          *tkParent,  
   [out] PCCOR_SIGNATURE  *ppvSigBlob,
   [out] ULONG            *pcbSigBlob  
);
```  
  
## <a name="parameters"></a>参数  

 `mi`  
 中一个 MethodSpec 标记，表示方法的实例化。  
  
 `tkParent`  
 弄一个指针，指向表示方法定义的 MethodDef 或 MethodRef 标记。  
  
 `ppvSigBlob`  
 弄指向方法的二进制元数据签名的指针。  
  
 `pcbSigBlob`  
 弄的大小（以字节为单位） `ppvSigBlob` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataImport2 接口](imetadataimport2-interface.md)
- [IMetaDataImport 接口](imetadataimport-interface.md)
