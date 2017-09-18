---
title: "Метод (SQLServerResultSet) rowInserted | Документы Microsoft"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- SQLServerResultSet.rowInserted
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: e7c10372-0be8-4baa-87f7-ed6b66003357
caps.latest.revision: 8
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 885d101c9f19cd416fa85155be74aabd72bdefff
ms.contentlocale: ru-ru
ms.lasthandoff: 09/09/2017

---
# <a name="rowinserted-method-sqlserverresultset"></a>rowInserted метод (SQLServerResultSet)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Возвращает значение, определяющее, была ли сделана вставка в текущую строку.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
  
public boolean rowInserted()  
```  
  
## <a name="return-value"></a>Возвращаемое значение  
 **значение true,** Если строка была выполнена вставка и обнаружены операции вставки. В противном случае — **false**.  
  
## <a name="exceptions"></a>Исключения  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Замечания  
 Этот метод rowUpdated указывается с помощью метода rowUpdated в интерфейсе java.sql.ResultSet.  
  
 Значение, которое возвращается зависит это [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md) возможности обнаружения видимых операций вставки объектом.  
  
> [!NOTE]  
>  [!INCLUDE[ssNoVersion](../../../includes/ssnoversion_md.md)]не обнаруживает вставленные строки для любого типа курсора.  
  
## <a name="see-also"></a>См. также:  
 [Элементы SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [Класс SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  