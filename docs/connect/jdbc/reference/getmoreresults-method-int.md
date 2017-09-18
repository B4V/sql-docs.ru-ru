---
title: "Метод getMoreResults (int) | Документы Microsoft"
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
- SQLServerStatement.getMoreResults (int)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 6419e5a8-8b3a-4d5b-8226-95865c52c723
caps.latest.revision: 10
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 0daf7ce3684ce376ea228adcc9e4b2c0d32f831b
ms.contentlocale: ru-ru
ms.lasthandoff: 09/09/2017

---
# <a name="getmoreresults-method-int"></a>Метод getMoreResults (int)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Переходит к следующему результату [SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-class.md) объекта и сделками с какой-либо открытых результат задать объекты в соответствии с инструкциями, заданными указанным режимом.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
  
public final boolean getMoreResults(int mode)  
```  
  
#### <a name="parameters"></a>Параметры  
 *режим*  
  
 **Int** , указывающее способ обработки объекты открытые результирующего набора. Это должна быть одна из следующих констант:  
  
 CLOSE_CURRENT_RESULT  
  
 KEEP_CURRENT_RESULT (не поддерживается драйвером JDBC)  
  
 CLOSE_ALL_RESULTS  
  
## <a name="return-value"></a>Возвращаемое значение  
 **значение true,** если возвращенный результат является результирующим набором. В противном случае — **false**.  
  
## <a name="exceptions"></a>Исключения  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Замечания  
 Этот метод getMoreResults указывается с помощью метода getMoreResults в интерфейсе java.sql.Statement.  
  
 Если метод getMoreResults вызывается перед получением результатов, он ведет себя в соответствии с *режим* аргумента и переходит к следующему результату.  
  
> [!NOTE]  
>  Драйвер JDBC не поддерживает использование константы KEEP_CURRENT_RESULT. Если эта константа используется, вызывается исключение.  
  
## <a name="see-also"></a>См. также:  
 [Метод getMoreResults &#40; SQLServerStatement &#41;](../../../connect/jdbc/reference/getmoreresults-method-sqlserverstatement.md)   
 [Члены SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-members.md)   
 [Класс SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-class.md)  
  
  