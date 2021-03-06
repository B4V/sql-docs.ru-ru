---
title: Изменение свойств таблицы | Документы Майкрософт
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: conceptual
f1_keywords:
- editTabProps
ms.assetid: 95ea72ba-8e40-4177-a963-0fb4d10c56e3
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 4499ba0bc52e7c0d5cd052a8999737bf53337a50
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2018
ms.locfileid: "47686972"
---
# <a name="edit-the-table-properties"></a>Изменение свойств таблицы
  Это диалоговое окно служит для изменения столбцов из выбранной таблицы, для которой производится отслеживание изменений. Можно также изменить **Роль безопасности** и **Экземпляр отслеживания** .  
  
### <a name="to-edit-the-columns-to-include-in-the-cdc-instance"></a>Изменение столбцов, включаемых в экземпляр CDC  
  
1.  Выполните одно из следующих действий (или оба).  
  
    -   Установите флажки для всех дополнительных столбцов, которые необходимо включить.  
  
    -   Снимите флажки для тех столбцов, которые необходимо исключить.  
  
### <a name="to-edit-the-security-role"></a>Изменение роли безопасности  
  
1.  Введите новое имя или измените имя роли безопасности в поле **Роль безопасности** .  
  
### <a name="to-create-a-new-capture-instance"></a>Создание нового экземпляра отслеживания  
  
1.  В разделе **Роль безопасности** введите имя экземпляра отслеживания в поле **Имя** . По умолчанию в этом поле указано имя текущего экземпляра отслеживания, в конец которого добавляется суффикс **_NEW** (например, **старый_экземпляр_NEW**).  
  
2.  Сохраните экземпляр отслеживания как один из следующих вариантов.  
  
    -   **Новый экземпляр отслеживания**. В этом случае новый экземпляр отслеживания сохраняется, а старый не удаляется.  
  
         **Примечание**. Для одной таблицы может быть не больше двух экземпляров отслеживания. Если уже есть два экземпляра отслеживания, то этот вариант будет недоступен.  
  
    -   **Замена существующего экземпляра**. В этом случае текущий экземпляр отслеживания удаляется и заменяется созданным экземпляром. Если для этой таблицы уже созданы два экземпляра отслеживания, то необходимо выбрать один из них для замены.  
  
 **Примечание**. Экземпляр отслеживания можно удалить из списка таблиц на вкладке **Таблица** .  
  
 После окончания ввода данных в этом диалоговом окне нажмите кнопку **ОК** , чтобы принять изменения.  
  
## <a name="see-also"></a>См. также:  
 [Как изменить свойства экземпляра CDC](../../integration-services/change-data-capture/how-to-edit-the-cdc-instance-properties.md)   
 [Внесение изменений в выбранные для отслеживания изменений таблицы](../../integration-services/change-data-capture/make-changes-to-the-tables-selected-for-capturing-changes.md)  
  
  
