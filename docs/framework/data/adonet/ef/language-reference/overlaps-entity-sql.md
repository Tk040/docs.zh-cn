---
description: '了解详细信息： (实体 SQL 重叠) '
title: OVERLAPS (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 41743e89-79cb-4d7b-8a27-355b45024b61
ms.openlocfilehash: dd2f4a0925c57edcc3dd2d1264d00921b092525a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791902"
---
# <a name="overlaps-entity-sql"></a>OVERLAPS (Entity SQL)

确定两个集合是否具有公共元素。  
  
## <a name="syntax"></a>语法  
  
```sql  
expression OVERLAPS expression  
```  
  
## <a name="arguments"></a>参数  

 `expression`  
 返回一个集合以与从其他查询表达式返回的集合进行比较的任何有效查询表达式。 所有表达式都必须与 `expression`一样属于同一类型或属于公共基类型或派生类型。  
  
## <a name="return-value"></a>返回值  

 如果两个集合具有公共元素，则为`true` ；否则为 `false`。  
  
## <a name="remarks"></a>备注  

 重叠提供的功能等效于以下形式：  
  
 `EXISTS ( expression INTERSECT expression )`  
  
 OVERLAPS 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符之一。 所有 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符都是从左到右进行求值。 有关集运算符的优先级信息 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] ，请参阅 [EXCEPT](except-entity-sql.md)。  
  
## <a name="example"></a>示例  

 以下 Entity SQL 查询使用 OVERLAPS 运算符以确定两个集合是否具有公共值。 此查询基于 AdventureWorks 销售模型。 若要编译并运行此查询，请执行下列步骤：  
  
1. 执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。  
  
2. 将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：  
  
 [!code-sql[DP EntityServices Concepts#OVERLAPS](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#overlaps)]  
  
## <a name="see-also"></a>请参阅

- [实体 SQL 引用](entity-sql-reference.md)
