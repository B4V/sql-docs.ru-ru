---
title: catalog.create_environment (база данных SSISDB) | Документы Майкрософт
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: language-reference
ms.assetid: 66367092-9f6e-40e6-90bd-81efb078ab70
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 3b0ff9e5c2a5874b5ff01e8da19fa6015e28b5e2
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2018
ms.locfileid: "47778562"
---
# <a name="catalogcreateenvironment-ssisdb-database"></a>catalog.create_environment (база данных SSISDB)
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  Создает среду в каталоге служб [!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)].  
  
## <a name="syntax"></a>Синтаксис  
  
```sql  
catalog.create_environment [@folder_name =] folder_name  
     , [@environment_name =] environment_name  
  [  , [@environment_description =] environment_description ]  
```  
  
## <a name="arguments"></a>Аргументы  
 [@folder_name =] *folder_name*  
 Имя папки, которая будет содержать среду. Параметр *folder_name* имеет тип **nvarchar(128)**.  
  
 [@environment_name =] *environment_name*  
 Имя среды. Параметр *environment_name* имеет тип **nvarchar(128)**.  
  
 [@environment_description=] *environment_description*  
 Необязательное описание среды. Параметр *environment_description* имеет тип **nvarchar(1024)**.  
  
## <a name="return-code-value"></a>Значения кодов возврата  
 0 (успешное завершение)  
  
## <a name="result-sets"></a>Результирующие наборы  
 None  
  
## <a name="permissions"></a>Разрешения  
 Эта хранимая процедура требует применения одного из следующих разрешений:  
  
-   Разрешения READ и MODIFY на папку  
  
-   Членство в роли базы данных **ssis_admin**  
  
-   роль базы данных;  
  
-   Членство в роли сервера **sysadmin**  
  
## <a name="errors-and-warnings"></a>Ошибки и предупреждения  
 Следующий список содержит описания некоторых условий, которые могут вызвать ошибку или предупреждение.  
  
-   Имя папки не обнаружено  
  
-   Среда с таким именем уже существует в указанной папке  
  
## <a name="remarks"></a>Remarks  
 Имя среды должно быть уникальным в пределах папки.  
  
  
