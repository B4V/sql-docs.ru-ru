---
title: "Элемент ScriptCacheProcessingMode (ASSL) | Документы Microsoft"
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
apiname:
- ScriptCacheProcessingMode Element
apilocation:
- http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to:
- SQL Server 2016 Preview
f1_keywords:
- ScriptCacheProcessingMode
helpviewer_keywords:
- ScriptCacheProcessingMode element
ms.assetid: 95c0723c-69a4-43e7-b743-f712180a7681
caps.latest.revision: 33
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 1982cc5b9266f8d69d0975043c307ec3272d8149
ms.contentlocale: ru-ru
ms.lasthandoff: 09/01/2017

---
# <a name="scriptcacheprocessingmode-element-assl"></a>Элемент ScriptCacheProcessingMode (ASSL)
  Указывает, должен ли сервер строить кэш скриптов во время или после обработки.  
  
## <a name="syntax"></a>Синтаксис  
  
```xml  
  
<Cube>  
   ...  
      <ScriptCacheProcessingMode>...</ScriptCacheProcessingMode>  
   ...  
</Cube>  
```  
  
## <a name="element-characteristics"></a>Характеристики элемента  
  
|Характеристика|Описание|  
|--------------------|-----------------|  
|Тип данных и длина|String (перечисление)|  
|Значение по умолчанию|*Обычный*|  
|Количество элементов|0—1: необязательный элемент, который может появляться только один раз.|  
  
## <a name="element-relationships"></a>Связи элемента  
  
|Связь|Элемент|  
|------------------|-------------|  
|Родительский элемент|[Cube](../../../analysis-services/scripting/objects/cube-element-assl.md)|  
|Дочерние элементы|None|  
  
## <a name="remarks"></a>Замечания  
 Значением этого элемента может быть только одна из строк в следующей таблице.  
  
|Значение|Description|  
|-----------|-----------------|  
|*Обычный*|Сервер создает кэш скрипта во время обработки.|  
|*Отложенная*|Сервер создает кэш скрипта после обработки.|  
  
 Перечисление, соответствующее разрешенным значениям для **ScriptCacheProcessingMode** в модели объектов Analysis Management объекты AMO — <xref:Microsoft.AnalysisServices.ScriptCacheProcessingMode>.  
  
 Элемент, соответствующий родителю параметра **ScriptCacheProcessingMode** в модели объектов Analysis Management объекты AMO — <xref:Microsoft.AnalysisServices.Cube>.  
  
## <a name="see-also"></a>См. также:  
 [Свойства &#40; ASSL &#41;](../../../analysis-services/scripting/properties/properties-assl.md)  
  
  