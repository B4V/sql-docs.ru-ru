---
title: "Занятие 5: Создание связей | Документы Microsoft"
ms.custom: 
ms.date: 03/27/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
ms.tgt_pltfrm: 
ms.topic: get-started-article
applies_to:
- SQL Server 2016
ms.assetid: abac1a00-f827-4c3e-a473-6db5c8a3a66f
caps.latest.revision: 29
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 096f19dc25973b2d515c6ccfb9961e7b0fe07c21
ms.contentlocale: ru-ru
ms.lasthandoff: 09/01/2017

---
# <a name="lesson-4-create-relationships"></a>Занятие 4. Создание связей
[!INCLUDE[ssas-appliesto-sql2016-later-aas](../includes/ssas-appliesto-sql2016-later-aas.md)]

На этом занятии будут проверены связи, которые были автоматически созданы во время импорта данных и добавить новые связи между различными таблицами. Связь — это соединение между двумя таблицами, которое определяет, каким образом должны соотноситься данные этих таблиц. Например, таблица DimProduct и таблица DimProductSubcategory содержат связь на основе того факта, что каждый продукт принадлежит подкатегории. Дополнительные сведения см. в разделе [связи](../analysis-services/tabular-models/relationships-ssas-tabular.md).
  
Предполагаемое время выполнения данного занятия: **10 минут.**  
  
## <a name="prerequisites"></a>Предварительные требования  
Этот раздел является частью учебника по табличному моделированию, который необходимо изучать по порядку. Перед выполнением задач этого занятия, необходимо завершить предыдущее занятие: [занятия 3: пометить как таблицу дат](../analysis-services/lesson-3-mark-as-date-table.md). 
  
## <a name="review-existing-relationships-and-add-new-relationships"></a>Обзор существующих связей и добавление новых  
Во время импорта данных с помощью мастера импорта таблиц, полученный семь таблиц из базы данных AdventureWorksDW. Как правило при импорте данных из реляционного источника существующие связи автоматически импортируются вместе с данными. Однако необходимо проверить правильность создания связей между таблицами, прежде чем продолжить создание модели. В этом учебнике будут также созданы три новые связи.  
  
#### <a name="to-review-existing-relationships"></a>Просмотр существующих связей  
  
1.  Нажмите кнопку **модели** меню > **представление модели** > **представление диаграммы**.  

    Конструктор моделей появится в представлении диаграммы — графическом формате отображения всех импортированных таблиц, соединенных линиями. Линии между таблицами указывают на связи, которые были автоматически созданы во время импорта данных.
    
    ![как табличных lesson4-диаграмма](../analysis-services/media/as-tabular-lesson4-diagram.png)
  
    Используйте элементы управления мини-карты в правом нижнем углу конструктора моделей, чтобы настроить представление, включив в него как можно большее число таблиц. Можно также выбирать и перетаскивать таблицы в другие места. Например, их можно свести вместе или разместить в определенном порядке. Перемещение таблиц не влияет на связи между ними. Для просмотра всех столбцов в определенной таблице щелкните и перетащите край таблицы, чтобы увеличить или уменьшить ее.  
  
2.  Щелкните сплошную линию между **DimCustomer** таблицы и **DimGeography** таблицы. Сплошная линия между этими двумя таблицами показывает, что связь активна, то есть она используется по умолчанию при расчете DAX-формул.  
  
    Обратите внимание **GeographyKey** столбца в **DimCustomer** таблицы и **GeographyKey** столбца в **DimGeography** таблицы появились в поле. Это указывает на то, что эти столбцы используются в связи. Свойства связи также отображаются в окне **Свойства** .  
  
    > [!TIP]  
    > Помимо использования конструктора моделей в представлении диаграммы, можно также использовать диалоговое окно «Управление связями» для отображения связей между всеми таблицами в табличном формате. Щелкните правой кнопкой мыши **связи** в обозреватель табличной модели, а затем выберите **управление связями**. Диалоговое окно «Управление связями» показывает связи, которые были автоматически созданы во время импорта данных.  
  
3.  Используйте конструктор моделей в представлении диаграммы или диалоговое окно «Управление связями», чтобы убедиться, что следующие связи были созданы во время каждой из таблиц были импортированы из базы данных AdventureWorksDW.  
  
    |Активен|Таблица|Связанная таблица подстановки|  
    |----------|---------|------------------------|  
    |Да|**DimCustomer [GeographyKey]**|**DimGeography [GeographyKey]**|  
    |Да|**DimProduct [ProductSubcategoryKey]**|**DimProductSubcategory [ProductSubcategoryKey]**|  
    |Да|**DimProductSubcategory [ProductCategoryKey]**|**DimProductCategory [ProductCategoryKey]**|  
    |Да|**FactInternetSales [CustomerKey]**|**DimCustomer [CustomerKey]**|  
    |Да|**FactInternetSales [ProductKey]**|**DimProduct [ProductKey]**|  
  
    Если какие-либо связи в приведенной выше таблице отсутствуют, убедитесь, что модель включает следующие таблицы: DimCustomer, DimDate, DimGeography, DimProduct, DimProductCategory DimProductSubcategory и FactInternetSales. Если таблицы импортируются из одного подключения к источнику данных несколько раз, связи между этими таблицами не будут созданы и их нужно будет создавать вручную.  

### <a name="take-a-closer-look"></a>Более подробно
В представлении диаграммы можно заметить стрелки, звездочку и число строк, которые показывают связи между таблицами.

![как табличные lesson4-строки](../analysis-services/media/as-tabular-lesson4-line.png)

Стрелка показывает направление фильтра звездочка показано это таблица — сторону «многие» связи на количество элементов, а значение 1 показывает, что эта таблица составляет сторону «один» связи. Если нужно изменить связь. Например можно изменить направление фильтрации отношение или количество элементов, дважды щелкните линию связи в представлении диаграммы, чтобы открыть диалоговое окно Изменение отношения.

![как табличные lesson4-редактирования](../analysis-services/media/as-tabular-lesson4-edit.png)

Скорее всего никогда не потребуется изменить связь. Эти функции предназначены для моделирования данных и выходит за рамки данного руководства. Дополнительные сведения см. в разделе [двунаправленные кросс-фильтры для табличных моделей в SQL Server 2016 Analysis Services](../analysis-services/tabular-models/bi-directional-cross-filters-tabular-models-analysis-services.md).

В некоторых случаях может потребоваться создание дополнительных связей между таблицами в модели, чтобы поддержать определенную бизнес-логику. В этом учебнике необходимо создать три дополнительные связи между таблицами FactInternetSales и DimDate.  
  
#### <a name="to-add-new-relationships-between-tables"></a>Добавление новых связей между таблицами  
  
1.  В конструкторе моделей в **FactInternetSales** щелкните и удерживайте **OrderDate** столбец, затем перетащите курсор в **даты** столбца в  **DimDate** таблицы, а затем отпустите.  

    Появится сплошная линия, показывающая создана активная связь между **OrderDate** столбца в **продажи через Интернет** таблицы и **даты** столбца в **Дата** таблицы. 
  
      ![AS табличных lesson4-new](../analysis-services/media/as-tabular-lesson4-new.png) 
  
    > [!NOTE]  
    > При создании связи, количества элементов и фильтр направление между первичной таблицей и связанной таблицей поиска выбирается автоматически.  
  
2.  В **FactInternetSales** щелкните и удерживайте **DueDate** столбец, затем перетащите курсор в **даты** столбца в **DimDate** таблицы, а затем отпустите.  
  
    Появится пунктирная линия, показывающая создана неактивная связь между **DueDate** столбца в **FactInternetSales** таблицы и **даты** столбца в  **DimDate** таблицы. Между таблицами можно создавать несколько связей, но одновременно может быть активна только одна связь.  
  
3.  Наконец создайте еще одну связь; в **FactInternetSales** щелкните и удерживайте **ShipDate** столбец, затем перетащите курсор в **даты** столбца в **DimDate** Таблица, а затем отпустите.  
    
     ![как табличных lesson4-newinactive](../analysis-services/media/as-tabular-lesson4-newinactive.png)
  
## <a name="whats-next"></a>Дальнейшие действия
Перейдите к следующему занятию: [занятия 5: Создание вычисляемых столбцов](../analysis-services/lesson-5-create-calculated-columns.md).
  
  
  
