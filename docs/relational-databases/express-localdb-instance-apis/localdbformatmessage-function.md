---
title: Функция LocalDBFormatMessage | Документация Майкрософт
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology:
- database-engine
ms.topic: reference
apiname:
- LocalDBFormatMessage
apilocation:
- sqluserinstance.dll
apitype: DLLExport
ms.assetid: 31b3152a-94cf-4f75-a31b-296d7dd16dbe
author: CarlRabeler
ms.author: carlrab
manager: craigg
ms.openlocfilehash: 52a07ec8c2793116077cc88c6cb338befac2eee0
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2018
ms.locfileid: "47821302"
---
# <a name="localdbformatmessage-function"></a>Функция LocalDBFormatMessage
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  Возвращает локализованное текстовое описание для указанной ошибки SQL Server Express LocalDB.  
  
 **Файл заголовка:** sqlncli.h  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT LocalDBFormatMessage(  
           HRESULT hrLocalDB,  
           DWORD dwFlags,   
           DWORD dwLanguageId,   
           LPWSTR wszMessage,   
           LPDWORD lpcchMessage   
);  
```  
  
## <a name="parameters"></a>Параметры  
 *hrLocalDB*  
 [Вход] Код ошибки LocalDB.  
  
 *dwFlags*  
 [Вход] Флаги, задающие поведение этой функции.  
  
 Доступные флаги:  
  
 LOCALDB_TRUNCATE_ERR_MESSAGE  
 Если размер входного буфера окажется недостаточным, сообщение об ошибке урезается до длины буфера.  
  
 *dwLanguageId*  
 [Вход] Требуемый язык (LANGID) или значение 0. В последнем случае используется порядок языков Win32 FormatMessage.  
  
 *wszMessage*  
 [Выход] Буфер для сохранения сообщения об ошибке LocalDB.  
  
 *lpcchMessage*  
 [Вход/выход] На входе содержит размер буфера *wszMessage* в символах. На выходе, если указан недостаточный размер буфера, содержит требуемый размер буфера в символах, включая любые конечные символы NULL. При успешном завершении работы функции содержит количество символов в сообщении без учета конечных символов NULL.  
  
## <a name="returns"></a>Возвращает  
 S_OK  
 Функция выполнена успешно.  
  
 [LOCALDB_ERROR_NOT_INSTALLED](../../relational-databases/express-localdb-error-messages/localdb-error-not-installed.md)  
 Компонент SQL Server Express LocalDB не установлен на компьютере.  
  
 [LOCALDB_ERROR_INVALID_PARAMETER](../../relational-databases/express-localdb-error-messages/localdb-error-invalid-parameter.md)  
 Один или несколько указанных входных параметров недопустимы.  
  
 [LOCALDB_ERROR_UNKNOWN_ERROR_CODE](../../relational-databases/express-localdb-error-messages/localdb-error-unknown-error-code.md)  
 Запрошенное сообщение не существует.  
  
 [LOCALDB_ERROR_UNKNOWN_LANGUAGE_ID](../../relational-databases/express-localdb-error-messages/localdb-error-unknown-language-id.md)  
 Сообщение недоступно на запрошенном языке.  
  
 [LOCALDB_ERROR_INSUFFICIENT_BUFFER](../../relational-databases/express-localdb-error-messages/localdb-error-insufficient-buffer.md)  
 Размер входного буфера *wszMessage* недостаточный; усечение не было запрошено.  
  
 [LOCALDB_ERROR_INTERNAL_ERROR](../../relational-databases/express-localdb-error-messages/localdb-error-internal-error.md)  
 Произошла непредвиденная ошибка. Подробные сведения см. в журнале событий.  
  
## <a name="remarks"></a>Примечания  
 Образец кода, использующего API LocalDB, см. в разделе [SQL Server Express LocalDB Reference](../../relational-databases/sql-server-express-localdb-reference.md)  
  
## <a name="see-also"></a>См. также  
 [Заголовок и сведения о версии SQL Server Express LocalDB](../../relational-databases/express-localdb-instance-apis/sql-server-express-localdb-header-and-version-information.md)  
  
  
