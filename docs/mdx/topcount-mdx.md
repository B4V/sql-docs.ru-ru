---
title: "TopCount (многомерные Выражения) | Документы Microsoft"
ms.custom: 
ms.date: 03/02/2016
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- TOPCOUNT
dev_langs:
- kbMDX
helpviewer_keywords:
- TopCount function
ms.assetid: 15026a8f-35c5-4307-8856-348f5c44bfd5
caps.latest.revision: 32
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: 09b3d169600622822b2d3e5a78ad72c3164efcb9
ms.contentlocale: ru-ru
ms.lasthandoff: 08/02/2017

---
# <a name="topcount-mdx"></a>TopCount (многомерные выражения)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx_md](../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Сортирует набор по убыванию и возвращает заданное число элементов с самыми высокими значениями.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
  
TopCount(Set_Expression,Count [ ,Numeric_Expression ] )  
```  
  
## <a name="arguments"></a>Аргументы  
 *Set_Expression*  
 Допустимое многомерное выражение, возвращающее набор.  
  
 *Count*  
 Допустимое числовое выражение, указывающее количество возвращаемых кортежей.  
  
 *Numeric_Expression*  
 Допустимое числовое выражение (обычно многомерное выражение координат ячейки), возвращающее число.  
  
## <a name="remarks"></a>Замечания  
 Если числовое выражение указано, **TopCount** функция сортирует в порядке убывания кортежи в наборе указанный заданного набора по значениям числового выражения, вычисленного над заданным набором. После сортировки набора, **TopCount** затем функция возвращает заданное количество кортежей с самыми высокими значениями.  
  
> [!IMPORTANT]  
>  Как [BottomCount](../mdx/bottomcount-mdx.md) функции **TopCount** функция всегда нарушает иерархию.  
  
 Если числовое выражение не указано, функция возвращает набор элементов в естественном порядке без какой-либо сортировки аналогично [Head (MDX)](../mdx/head-mdx.md) функции.  
  
## <a name="examples"></a>Примеры  
 В следующем примере возвращается 10 дат с самыми высокими значениями по мере Internet Sales Amount:  
  
 `SELECT [Measures].[Internet Sales Amount] ON 0,`  
  
 `TOPCOUNT([Date].[Date].[Date].MEMBERS, 10, [Measures].[Internet Sales Amount])`  
  
 `ON 1`  
  
 `FROM [Adventure Works]`  
  
 В следующем примере из категории Bike возвращаются первые пять элементов набора, содержащего все сочетания элементов с уровнем City в иерархии Geography в измерении Geography и все финансовые годы из иерархии Fiscal измерения Date, отсортированные по мере Reseller Sales Amount (начиная с элементов этого набора с наибольшим объемом продаж).  
  
```  
SELECT [Measures].[Reseller Sales Amount] ON 0,  
TopCount  
   ({[Geography].[Geography].[City].Members   
      *[Date].[Fiscal].[Fiscal Year].Members}  
   , 5  
   , [Measures].[Reseller Sales Amount]  
   ) ON 1  
FROM [Adventure Works]  
WHERE([Product].[Product Categories].Bikes)  
```  
  
## <a name="see-also"></a>См. также:  
 [Справочник по функциям многомерных Выражений &#40; Многомерные Выражения &#41;](../mdx/mdx-function-reference-mdx.md)  
  
  
