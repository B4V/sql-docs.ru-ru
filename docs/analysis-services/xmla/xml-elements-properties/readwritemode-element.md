---
title: "Элемент ReadWriteMode | Документы Microsoft"
ms.custom: 
ms.date: 03/06/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
- docset-sql-devref
ms.tgt_pltfrm: 
ms.topic: reference
applies_to:
- SQL Server 2016 Preview
helpviewer_keywords:
- ReadWriteMode command
ms.assetid: 379bcaca-bb7e-4934-a9e7-21f8ede2fdc7
caps.latest.revision: 13
author: jeannt
ms.author: jeannt
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 3075b7834f7e24004811ce3802dd5fcb55b56f6c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/01/2017

---
# <a name="readwritemode-element"></a>Элемент ReadWriteMode
  Свойство базы данных **ReadWriteMode** указывает, в каком режиме работает база данных: **ReadWrite** или **ReadOnly** . Эти значения являются единственными допустимыми для данного свойства.  
  
## <a name="syntax"></a>Синтаксис  
  
```xml  
  
<Database>  
...  
   <ddlns_100_0:ReadWriteMode>...</ddlns_100_0:ReadWriteMode>  
...  
</Database>  
```  
  
## <a name="element-characteristics"></a>Характеристики элемента  
  
|Характеристика|Описание|  
|--------------------|-----------------|  
|Тип данных и длина|String (перечисление)|  
|Значение по умолчанию|ReadWrite|  
|Количество элементов|0—1: необязательный элемент, который может встречаться несколько раз.|  
  
## <a name="element-relationships"></a>Связи элемента  
  
|Связь|Элемент|  
|------------------|-------------|  
|Родительские элементы|[База данных](../../../analysis-services/xmla/xml-elements-properties/database-element-xmla.md)|  
|Дочерние элементы|None|  
  
## <a name="remarks"></a>Замечания  
 Базы данных создаются только в режиме **ReadWrite** . Базы данных не могут создаваться в режиме **ReadOnly** .  
  
 Значением элемента **ReadWriteMode** может быть только одна из строк в следующей таблице.  
  
|Значение|Description|  
|-----------|-----------------|  
|*Только для чтения*|База данных не может быть ни обновлена, ни изменена.|  
|*ReadWrite*|База данных может изменяться и обновляться.|  
  
## <a name="see-also"></a>См. также:  
 [Элемент Attach](../../../analysis-services/xmla/xml-elements-commands/attach-element.md)   
 [Присоединение и отсоединение баз данных служб Analysis Services](../../../analysis-services/multidimensional-models/attach-and-detach-analysis-services-databases.md)   
 [Перемещение базы данных служб Analysis Services](../../../analysis-services/multidimensional-models/move-an-analysis-services-database.md)   
 [Режимы ReadWriteModes базы данных](../../../analysis-services/multidimensional-models/database-readwritemodes.md)   
 [Переключение базы данных служб Analysis Services между режимами ReadOnly и ReadWrite](../../../analysis-services/multidimensional-models/switch-an-analysis-services-database-between-readonly-and-readwrite-modes.md)  
  
  