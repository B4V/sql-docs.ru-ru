---
title: Элемент EventString (DTA) | Документация Майкрософт
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- database-engine
ms.topic: conceptual
dev_langs:
- XML
helpviewer_keywords:
- EventString element
ms.assetid: f76c37b4-2f6e-4274-8ee2-87e89d98e8a2
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: 0ecfed53ebcecf38bbd46a6d3b15d1a8a8c741fe
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48156024"
---
# <a name="eventstring-element-dta"></a>Элемент EventString (DTA)
  Задает скрипт рабочей нагрузки [!INCLUDE[tsql](../../includes/tsql-md.md)] непосредственно во входном XML-файле.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
  
<Workload>  
    <EventString Weight="...">  
    ...code removed here...  
    </EventString>  
</Workload>  
```  
  
## <a name="element-attributes"></a>Атрибуты элемента  
  
|attribute|Описание|  
|---------------|-----------------|  
|`Weight`|Необязательный параметр. Задает весовой коэффициент запроса (коэффициент важности) для указанного события. Используйте `float` тип данных, чтобы задать вес. Например, `Weight`="100,01". Минимальное значение, которое можно задать для коэффициента `Weight`, равно 0.|  
  
## <a name="element-characteristics"></a>Характеристики элемента  
  
|Характеристика|Описание|  
|--------------------|-----------------|  
|**Тип данных и длина**|`string`, длина не ограничена.|  
|**Значение по умолчанию**|Нет.|  
|**Наличие**|Необходимо наличие одного такого элемента, если не задан никакой другой тип рабочей нагрузки. Необходимо указать `EventString`, `File`, или `Database` дочернего элемента для `Workload` родительского, но только один тип может использоваться. Например, если рабочая нагрузка с `EventString` элемент, то также нельзя задавать рабочую нагрузку элементом `File` элемент в том же входном XML-файле.|  
  
## <a name="element-relationships"></a>Связи элемента  
  
|Связь|Элементы|  
|------------------|--------------|  
|**Родительский элемент**|[Элемент Workload &#40;DTA&#41;](workload-element-dta.md)|  
|**Дочерние элементы**|Нет.|  
  
## <a name="example"></a>Пример  
 Пример использования этого элемента см. в разделе [Образец входного XML-файла с описанием встроенной рабочей нагрузки (DTA)](xml-input-file-sample-with-inline-workload-dta.md).  
  
## <a name="see-also"></a>См. также  
 [Справочник по входным XML-файлам (помощник по настройке ядра СУБД)](xml-input-file-reference-database-engine-tuning-advisor.md)  
  
  
