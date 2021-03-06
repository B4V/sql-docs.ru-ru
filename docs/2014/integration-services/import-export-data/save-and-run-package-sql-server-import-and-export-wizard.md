---
title: Сохранение и выполнение пакета (мастер экспорта и импорта SQL Server) | Документация Майкрософт
ms.custom: ''
ms.date: 06/14/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- integration-services
ms.topic: conceptual
f1_keywords:
- sql12.dts.impexpwizard.saveschedule.f1
ms.assetid: b582c462-3d7a-4a4c-a2a2-2c79fedab75a
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: de6560f7bc91a76652be5ca198a91c4ab9c1f1af
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48104513"
---
# <a name="save-and-execute-package-sql-server-import-and-export-wizard"></a>Сохранение и выполнение пакета (мастер экспорта и импорта SQL Server)
  Используйте **сохранение и выполнение пакета** диалоговое окно, чтобы запустить пакет немедленно, сохранить его для последующего запуска или оба.  
  
> [!NOTE]  
>  Если остановить пакет до его завершения, пакет не сохраняется, даже если вы выбрали **Сохранить** "флажок".  
  
 Дополнительные сведения о работе этого мастера см. в разделе [SQL Server Импорт и экспорт](import-and-export-data-with-the-sql-server-import-and-export-wizard.md). Дополнительные сведения о режимах запуска мастера, а также разрешения, необходимые для успешного запуска мастера, см. в разделе [запустить мастер экспорта и импорта SQL Server](start-the-sql-server-import-and-export-wizard.md).  
  
 Назначение мастера импорта и экспорта SQL Server заключается в копировании данных из исходного расположения в целевое. Этот мастер может также создать целевую базу данных и целевые таблицы. Однако если нужно скопировать несколько баз данных, таблиц или других объектов базы данных, следует использовать мастер копирования баз данных. Дополнительные сведения см. в статье [Use the Copy Database Wizard](../../relational-databases/databases/use-the-copy-database-wizard.md).  
  
## <a name="options"></a>Параметры  
 **Выполнить немедленно**  
 Этот параметр выбирается для немедленного запуска пакета.  
  
 **Сохранить пакет служб SSIS**  
 Сохранение пакета для последующего выполнения с параметром немедленного выполнения.  
  
> [!NOTE]  
>  В [!INCLUDE[ssExpress](../../includes/ssexpress-md.md)], параметр, чтобы сохранить пакет, созданный мастером недоступен.  
  
 **SQL Server**  
 Выберите этот параметр, чтобы сохранить пакет в [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] `msdb` базы данных.  
  
> [!NOTE]  
>  Этот параметр доступен только в том случае, если вы выбрали **Сохранение пакета служб SSIS** параметр.  
  
 **Файловая система**  
 При выборе этого параметра пакет сохраняется в файле с расширением DTSX.  
  
> [!NOTE]  
>  Этот параметр доступен только в том случае, если вы выбрали **Сохранение пакета служб SSIS** параметр.  
  
 **Уровень защиты пакета**  
 Выберите уровень защиты из списка.  
  
 Уровень защиты определяет метод защиты (пароль или ключ пользователя) и область защиты пакетов. Защита может охватывать все данные или только конфиденциальные данные. Сведения о требованиях и параметрах настройки защиты пакетов, см. в разделе [контроль доступа для конфиденциальных данных в пакетах](../security/access-control-for-sensitive-data-in-packages.md) и [Общие сведения о безопасности &#40;служб Integration Services&#41;](../security/security-overview-integration-services.md).  
  
> [!NOTE]  
>  Этот параметр доступен только в том случае, если вы выбрали **Сохранение пакета служб SSIS** параметр.  
  
 **Пароль**  
 Введите пароль.  
  
> [!NOTE]  
>  Этот параметр доступен только в том случае, если вы задали **уровень защиты пакета** двух параметров: **Шифровать конфиденциальные данные паролем** или **шифровать все данные паролем**.  
  
 **Введите пароль еще раз**  
 Введите пароль еще раз.  
  
> [!NOTE]  
>  Этот параметр доступен только в том случае, если вы задали **уровень защиты пакета** двух параметров: **Шифровать конфиденциальные данные паролем** или **шифровать все данные паролем**.  
  
## <a name="see-also"></a>См. также  
 [Запуск проектов и пакетов](../packages/run-integration-services-ssis-packages.md)   
 [Сохранение пакетов](../save-packages.md)  
  
  
