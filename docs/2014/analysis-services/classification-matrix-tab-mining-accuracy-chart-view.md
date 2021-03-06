---
title: Вкладка «классификации матрицы» (представление диаграммы точности интеллектуального анализа данных) | Документация Майкрософт
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- analysis-services
ms.topic: conceptual
f1_keywords:
- sql12.dm.miningmodeleditor.accuracychart.confusionmatrix.f1
ms.assetid: 85d5a047-d656-41e0-8a31-400271c2a620
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 1879e9ec4f2a6decf4168e7c49a5e81d3a043d29
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48154714"
---
# <a name="classification-matrix-tab-mining-accuracy-chart-view"></a>Вкладка «Матрица классификации» (представление диаграммы точности интеллектуального анализа данных)
  На вкладке **Матрица классификации** отображается матрица классификации для каждой выбранной модели в сетке моделей вкладки **Сопоставление столбцов** . Матрица классификации доступна только в случае, если прогнозируемый столбец, выбранный на вкладке **Сопоставление столбцов** , не является непрерывным. Подробное описание вкладки **Матрица классификации** см. в разделе [Testing and Validation &#40;Data Mining&#41;](data-mining/testing-and-validation-data-mining.md).  
  
## <a name="options"></a>Параметры  
 **Копировать**  
 Позволяет скопировать содержимое каждой матрицы классификации в буфер обмена.  
  
 **Подсчитывает для \<модели > на \< прогнозируемый столбец >**  
 Отображает матрицу классификации для каждой модели интеллектуального анализа данных в структуре интеллектуального анализа. Матрица содержит следующие столбцы:  
  
|Значение|Описание|  
|-----------|-----------------|  
|**Прогноз**|Содержит строку для каждого состояния прогнозируемого столбца.|  
|**\<состояния > (фактические)**|Столбец для каждого состояния прогнозируемого столбца. Если состояния строки и столбца совпадают, в ячейке отображается фактическое число вхождений данного состояния в базе данных. Если они не совпадают, в ячейке отображается ошибка прогноза.|  
  
## <a name="see-also"></a>См. также  
 [Конструктор диаграммы точности интеллектуального &#40;интеллектуального анализа данных&#41;](mining-accuracy-chart-designer-data-mining.md)   
 [Тестирование и проверка задачи и инструкции по &#40;интеллектуального анализа данных&#41;](data-mining/testing-and-validation-tasks-and-how-tos-data-mining.md)   
 [Тестирование и проверка &#40;интеллектуального анализа данных&#41;](data-mining/testing-and-validation-data-mining.md)  
  
  
