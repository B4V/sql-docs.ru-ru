---
title: "Метод getUserName (SQLServerDatabaseMetaData) | Документы Microsoft"
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
- SQLServerDatabaseMetaData.getUserName
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 1ae81034-5de3-4f4a-b3f2-7d9d198a73af
caps.latest.revision: 7
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: e07e8540c432d1169684682eff975744c3412a31
ms.contentlocale: ru-ru
ms.lasthandoff: 09/09/2017

---
# <a name="getusername-method-sqlserverdatabasemetadata"></a>Метод getUserName (SQLServerDatabaseMetaData)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Возвращает имя пользователя, как оно известно в базе данных.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
  
public java.lang.String getUserName()  
```  
  
## <a name="return-value"></a>Возвращаемое значение  
 Объект **строка** , содержащее имя пользователя.  
  
## <a name="exceptions"></a>Исключения  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Замечания  
 Этот метод getUserName указывается с помощью getUserName метода в интерфейсе java.sql.DatabaseMetaData.  
  
## <a name="see-also"></a>См. также:  
 [Методы SQLServerDatabaseMetaData](../../../connect/jdbc/reference/sqlserverdatabasemetadata-methods.md)   
 [Элементы SQLServerDatabaseMetaData](../../../connect/jdbc/reference/sqlserverdatabasemetadata-members.md)   
 [Класс SQLServerDatabaseMetaData](../../../connect/jdbc/reference/sqlserverdatabasemetadata-class.md)  
  
  