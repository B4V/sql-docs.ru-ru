---
title: ~ (битовое НЕ) (выражение служб SSIS) | Документы Майкрософт
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- integration-services
ms.topic: conceptual
helpviewer_keywords:
- bitwise NOT (~)
- ~ (bitwise NOT)
ms.assetid: e4413ddd-0d0e-40c3-9c76-b5ce323218ec
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 655f09c1470e37f7d1503e1e3d151a734210e45c
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48154326"
---
# <a name="-bitwise-not-ssis-expression"></a>~ (битовое НЕ) (выражение служб SSIS)
  Выполняет битовую инверсию целого числа. Этот оператор может быть применен к целочисленному типу данных со знаком или без знака.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
  
~integer_expression  
  
```  
  
## <a name="arguments"></a>Аргументы  
 *integer_expression*  
 Любое допустимое выражение целочисленного типа данных. *integer*_*expression* — целое число, которое преобразуется в двоичное число для побитовой операции. Дополнительные сведения см. в статье [Integration Services Data Types](../data-flow/integration-services-data-types.md).  
  
## <a name="result-types"></a>Типы результата  
 Возвращает тип данных *integer_expression*.  
  
## <a name="remarks"></a>Примечания  
 None  
  
## <a name="expression-examples"></a>Примеры выражений  
 Этот пример выполняет операцию битового ~ (NOT) над числом 170 (0000 0000 1010 1010). Число целого типа со знаком.  
  
```  
  
~ 170  
```  
  
 Результат вычисления выражения — 170 (1111111101010101).  
  
 0000000010101010  
  
 ---------------------\-  
  
 1111111101010101  
  
## <a name="see-also"></a>См. также  
 [Приоритет и ассоциативность операторов](operator-precedence-and-associativity.md)   
 [Операторы &#40;выражение служб SSIS&#41;](operators-ssis-expression.md)  
  
  
