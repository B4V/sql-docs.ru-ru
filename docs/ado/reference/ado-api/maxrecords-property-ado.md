---
title: "Свойство MaxRecords (ADO) | Документы Microsoft"
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
apitype: COM
f1_keywords:
- Recordset15::MaxRecords
helpviewer_keywords:
- MaxRecords property [ADO]
ms.assetid: 20c76571-8c9a-482c-a99e-726ab1d93f8b
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 232f515c2250e1ec40fbb28bdff767baf9cf81c5
ms.contentlocale: ru-ru
ms.lasthandoff: 09/09/2017

---
# <a name="maxrecords-property-ado"></a>Свойство MaxRecords (ADO)
Указывает максимальное число записей, чтобы вернуться к [записей](../../../ado/reference/ado-api/recordset-object-ado.md) из запроса.  
  
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения  
 Возвращает или задает **длинные** значение, указывающее максимальное количество возвращаемых записей. По умолчанию равно нулю (**0**), что означает отсутствие ограничений.  
  
## <a name="remarks"></a>Замечания  
 Используйте **MaxRecords** свойство, чтобы ограничить количество записей, поставщик возвращает из источника данных. Значение по умолчанию этого свойства равно нулю, это означает, что поставщик возвращает все запрошенные записей.  
  
 **MaxRecords** свойство доступно для чтения/записи при **записей** будет закрыто, только для чтения при открытом.  
  
## <a name="applies-to"></a>Объект применения  
 [Объект набора записей (ADO)](../../../ado/reference/ado-api/recordset-object-ado.md)  
  
## <a name="see-also"></a>См. также:  
 [Пример свойства MaxRecords (Visual Basic)](../../../ado/reference/ado-api/maxrecords-property-example-vb.md)   
 [Пример свойства MaxRecords (VC ++)](../../../ado/reference/ado-api/maxrecords-property-example-vc.md)   
