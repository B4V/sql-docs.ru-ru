---
title: "sqlsrv_close | Документы Microsoft"
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
- sqlsrv_close
apitype: NA
helpviewer_keywords:
- sqlsrv_close
- API Reference, sqlsrv_close
ms.assetid: 6ac6209c-a134-4f8f-b88b-8eefaa1cbc7f
caps.latest.revision: 25
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: ab9135195867a02dccf3885b551ab2a1f4f5ebb1
ms.contentlocale: ru-ru
ms.lasthandoff: 09/09/2017

---
# <a name="sqlsrvclose"></a>sqlsrv_close
[!INCLUDE[Driver_PHP_Download](../../includes/driver_php_download.md)]

Закрывает указанное подключение и освобождает связанные ресурсы.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
  
sqlsrv_close( resource $conn )  
```  
  
#### <a name="parameters"></a>Параметры  
*$conn*: закрываемое подключение.  
  
## <a name="return-value"></a>Возвращаемое значение  
Логическое значение **true** , если только функция не вызывается с недопустимым параметром. Если функция вызывается с недопустимым параметром, возвращается значение **false** .  
  
> [!NOTE]  
> **Null** является допустимым параметром для этой функции. Это позволяет несколько раз вызывать функцию в скрипте. Например, если закрыть подключение с условием ошибки и закрыть его снова в конце скрипта, второй вызов **sqlsrv_close** вернет **true** , так как первый вызов **sqlsrv_ Закройте** (при возникновении ошибки) устанавливает для ресурса подключения **null**.  
  
## <a name="example"></a>Пример  
В следующем примере выполняется закрытие подключения. В примере предполагается, что SQL Server установлен на локальном компьютере. При выполнении примера из командной строки все выходные данные выводятся в консоль.  
  
```  
<?php  
/*Connect to the local server using Windows Authentication and   
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$conn = sqlsrv_connect( $serverName);  
if( $conn === false )  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
//-----------------------------------------------  
// Perform operations with connection here.  
//-----------------------------------------------  
  
/* Close the connection. */  
sqlsrv_close( $conn);  
echo "Connection closed.\n";  
?>  
```  
  
## <a name="see-also"></a>См. также:  
[Справочник по API для драйвера SQLSRV](../../connect/php/sqlsrv-driver-api-reference.md)  
[Информация о примерах кода в документации](../../connect/php/about-code-examples-in-the-documentation.md)  
  
