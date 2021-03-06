---
title: Создание, изменение и удаление моментальных снимков в журнале отчетов | Документы Майкрософт
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- reporting-services-native
ms.topic: conceptual
helpviewer_keywords:
- snapshots [Reporting Services]
- report snapshots [Reporting Services]
ms.assetid: 5aebbbfa-a8db-462d-8ab9-746fad9525f0
author: markingmyname
ms.author: maghan
manager: craigg
ms.openlocfilehash: 2d72c7991f1ebcf36a3408af344225967c1dc498
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48144704"
---
# <a name="create-modify-and-delete-snapshots-in-report-history"></a>Создание, изменение и удаление моментальных снимков в журнале отчетов
  Журнал отчета — это коллекция моментальных снимков отчета. Журнал отчета можно изменять, добавляя и удаляя моментальные снимки или редактируя свойства, от которых зависит его сохранение. Журнал отчета может быть создан вручную или по расписанию.  
  
 Для создания журнала отчета назначение роли должно включать задачу «Управление журналом отчета». Для просмотра журнала отчета назначение роли должно включать задачу «Просмотр отчетов». Журнал отчета доступен всем пользователям, которым доступен сам отчет. Нельзя выборочно предоставлять или закрывать доступ части пользователей.  
  
 Моментальные снимки в журнале отчетов идентифицируются по дате и времени создания. которые отражают момент выполнения запроса.  
  
## <a name="creating-snapshots-in-report-history"></a>Создание моментальных снимков в журнале отчета  
 Моментальные снимки можно создавать вручную или по расписанию для любого запроса, который может запускаться автоматически. Для автоматического запуска отчет должен использовать сохраненные учетные данные или не использовать их вовсе. Более того, если отчет использует параметры, их необходимо при запуске отчета установить в значения по умолчанию. Сохраненные учетные данные и значения параметров можно определить на страницах свойств отчета. Дополнительные сведения см. в разделе [Страница "Свойства параметров" (диспетчер отчетов)](../parameters-properties-page-report-manager.md).  
  
 При создании моментального снимка отчета вместе с ним в базе данных сервера отчетов сохраняются следующие элементы.  
  
-   Результирующий набор (данные отчета, полученные с использованием учетных данных, указанных на странице свойств «Источники данных» отчета).  
  
-   Определение базового отчета на момент создания моментального снимка. Если определение отчета после создания моментального снимка изменилось, эти изменения на моментальном снимке не отразятся.  
  
-   Значения параметров, использованные при получении или фильтрации результирующего набора.  
  
-   Внедренные ресурсы (например, изображения). Связанные с отчетом внешние ресурсы вместе с моментальным снимком отчета не сохраняются.  
  
 C помощью параметров указывается способ создания журнала отчета и количество его моментальных снимков, которые можно сохранить.  
  
 Если отчет порождает ошибку, моментальный снимок не создается. Отчеты, которые выводят предупреждения, но выполняются успешно, могут быть использованы для создания моментальных снимков.  
  
## <a name="modifying-properties-and-deleting-report-history"></a>Изменение свойств и удаление журнала отчета  
 Созданный моментальный снимок отчета изменять нельзя, но можно изменить его свойства таким образом, что журнал отчета будет удален.  
  
 Журнал отчета можно удалить следующими способами.  
  
-   Вручную удалить моментальные снимки по одному или группами.  
  
     Удалить моментальные снимки можно на странице «Журнал» диспетчера отчетов. Перейдите к отчету, нажмите «Журнал», установите флажки напротив соответствующих моментальных снимков и нажмите **Удалить**.  
  
-   Уменьшите предельный размер журнала отчета, чтобы ограничить число сохраняемых моментальных снимков. Предельный размер журнала может быть задан для отдельных отчетов или для сервера отчетов в целом. Если предельный размер уменьшается, из журнала отчета удаляются самые старые моментальные снимки.  
  
 Удалить хранящийся на сервере журнал отчета целиком при помощи массовой операции нельзя.  
  
 Но весь журнал целиком удаляется при удалении отчета. Например, при удалении месячного отчета по продажам по причине замещения его более новой версией, весь связанный с отчетом журнал будет утрачен. Однако при перемещении отчета весь журнал перемещается вместе с ним.  
  
## <a name="see-also"></a>См. также  
 [Создание журнала отчета &#40;режим интеграции служб Reporting Services в SharePoint&#41;](create-report-history-reporting-services-in-sharepoint-integrated-mode.md)   
 [Диспетчер отчетов &#40;собственный режим служб SSRS&#41;](../report-manager-ssrs-native-mode.md)   
 [Управление содержимым сервера отчетов &#40;собственный режим служб SSRS&#41;](report-server-content-management-ssrs-native-mode.md)   
 [Добавление моментального снимка к журналу отчета &#40;диспетчера отчетов&#41;](add-a-snapshot-to-report-history-report-manager.md)   
 [Ограничение размеров журнала отчета (диспетчер отчетов)](../reports/limit-report-history-report-manager.md)  
  
  
