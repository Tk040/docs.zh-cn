---
description: 了解详细信息： BC30712：无法加载类的信息<classname>
title: 无法加载类“<classname>”的信息
ms.date: 07/20/2015
f1_keywords:
- vbc30712
- bc30712
helpviewer_keywords:
- BC30712
ms.assetid: c7ffbd6d-05c6-4261-b44b-1bcd521bb350
ms.openlocfilehash: 5e96df57b83b32b70a2d0d6eca1578b5d15ec065
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674826"
---
# <a name="bc30712-unable-to-load-information-for-class-classname"></a>BC30712：无法加载类 "" 的信息 \<classname>

对不提供的类进行了引用。

 **错误 ID：** BC30712

## <a name="to-correct-this-error"></a>更正此错误

1. 验证是否定义了类，并且是否正确拼写了名称。

2. 尝试访问该模块中声明的其中一个成员。 在某些情况下，调试环境找不到成员，因为尚未加载在其中声明成员的模块。

## <a name="see-also"></a>请参阅

- [在 Visual Studio 中进行调试](/visualstudio/debugger/debugger-feature-tour)
