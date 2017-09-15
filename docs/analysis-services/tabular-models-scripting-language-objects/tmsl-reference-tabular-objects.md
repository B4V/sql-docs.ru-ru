---
title: "Определения объектов в табличной модели язык сценариев (TMSL) | Документы Microsoft"
ms.custom:
- SQL2016_New_Updated
ms.date: 05/30/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
- docset-sql-devref
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 486f0507-cec6-4672-b947-0bb61d1cbc46
caps.latest.revision: 11
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 3f69f6b59054b7fb1880757271b290874448373d
ms.contentlocale: ru-ru
ms.lasthandoff: 09/01/2017

---
# <a name="tmsl-reference---tabular-objects"></a>Ссылка TMSL - табличных объектов

[!INCLUDE[ssas-appliesto-sql2016-later-aas](../../includes/ssas-appliesto-sql2016-later-aas.md)]

  Приложения, создание, использование и администрирование табличных баз данных или, подключитесь к экземпляру SQL Sever 2016 Analysis Services в табличном режиме, могут использовать табличной модели языка скриптов (TMSL) для команд и представления объектов в формате JSON.  
  
 В этой статье приведены основные объекты схемы TMSL, используемых в скриптах, созданных SQL Server Management Studio, SQL Server Data Tools (SSDT) и объекты AMO PowerShell.  
  
 Определения объектов в формате JSON и используются в TMSL команды Create, Alter и удалить. В разделе [команд в табличной модели язык сценариев &#40; TMSL &#41; ](../../analysis-services/tabular-models-scripting-language-commands/tmsl-reference-commands.md) список команд.  
  
## <a name="main-objects"></a>Основные объекты  
 В следующей таблице приведен список наиболее часто используемых объектов в сценарии TMSL.  
  
|||  
|-|-|  
|[Объект базы данных &#40; TMSL &#41;](../../analysis-services/tabular-models-scripting-language-objects/database-object-tmsl.md)|Определяет табличной базы данных на уровне совместимости 1200 или выше, на основе модели одного уровня.|  
|[Объект модели &#40; TMSL &#41;](../../analysis-services/tabular-models-scripting-language-objects/model-object-tmsl.md)|Определяет табличной модели на уровне совместимости 1200 или выше.|  
|[Объект источника данных &#40; TMSL &#41;](../../analysis-services/tabular-models-scripting-language-objects/datasources-object-tmsl.md)|Определяет соединение с источником данных, используемые при импорте, чтобы загрузить модель или запросы к серверу при использовании модели в режиме DirectQuery.|  
|[Объект Tables &#40; TMSL &#41;](../../analysis-services/tabular-models-scripting-language-objects/tables-object-tmsl.md)|Указывает таблицы модели.|  
|[Объект секций &#40; TMSL &#41;](../../analysis-services/tabular-models-scripting-language-objects/partitions-object-tmsl.md)|Определяет хранилище строк таблицы, а также вычисляемые таблицы.|  
|[Объект связи &#40; TMSL &#41;](../../analysis-services/tabular-models-scripting-language-objects/relationships-object-tmsl.md)|Определяет связи между таблицами.|  
|[Объект роли &#40; TMSL &#41;](../../analysis-services/tabular-models-scripting-language-objects/roles-object-tmsl.md)|Определяет разрешения, членство и фильтры безопасности, управляющие доступом к данным и операциям.|  
  
## <a name="see-also"></a>См. также:  
 [Справочник по языку TMSL (Tabular Model Scripting Language)](../../analysis-services/tabular-model-scripting-language-tmsl-reference.md)  
  
  