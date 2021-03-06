---
title: Точечная диаграмма (службы Analysis Services — Интеллектуальный анализ данных) | Документация Майкрософт
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- analysis-services
ms.topic: conceptual
helpviewer_keywords:
- charts [Analysis Services]
- mining models [Analysis Services], validating
- scatter charts
- regression algorithms [Analysis Services]
ms.assetid: 166812ec-fd1c-47c8-88db-d5041142be91
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 5135fa8ed6565096e8e2cf5ff851c3c0c2aced72
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48179174"
---
# <a name="scatter-plot-analysis-services---data-mining"></a>Точечная диаграмма (службы Analysis Services — интеллектуальный анализ данных)
  На *точечной диаграмме* реальные значения пользовательских данных графически сравниваются с прогнозируемыми значениями в модели. Реальные значения отображаются на оси Х точечной диаграммы; прогнозируемые значения — на оси Y. На ней также отображается линия, отображающая идеальный прогноз, на которой прогнозируемое значение точно совпадает с реальным значением. Расстояние от точки на линии идеальных прогнозов, расположенной под углом в 45 градусов, показывает, насколько хорошо или плохо был выполнен прогноз.  
  
## <a name="understanding-the-scatter-plot"></a>Основные сведения о точечной диаграмме  
 Рассмотрим модель, при помощи которой в отделе маркетинга компании выполняется прогноз ежедневных продаж, основываясь на количестве переходов по ссылке, отправленной в рекламном электронном письме. Поскольку количество переходов и объем продаж являются непрерывными числовыми значениями, количество переходов можно представить на диаграмме как независимую переменную, а продажи — как зависимую. Прямая линия при этом показывает ожидаемую линейную связь, а точки, рассеянные вокруг линии, показывают, насколько реальные данные отличаются от ожидаемых. С помощью данного анализа можно визуально определить то, насколько набор результатов связан с определенным входом, а также то, насколько велико отклонение от идеальной модели.  
  
## <a name="interpreting-the-results"></a>Интерпретация результатов  
 Далее показывается пример точечной диаграммы, созданной для сценария, приведенного ранее.  
  
 ![Пример точечной диаграммы для линейной регрессии](../media/scatterplot-callctr.gif "пример точечной диаграммы для линейной регрессии")  
  
 Остановив указатель мыши над любой из точек, разбросанных на линии, можно увидеть в подсказке прогнозируемые и реальные значения. На точечной диаграмме отсутствуют **обозначения интеллектуального анализа данных** , однако сама диаграмма содержит условные обозначения, отражающие результаты, связанные с моделью. Дополнительные сведения об интерпретации этих результатов см. в разделе [Содержимое моделей интеллектуального анализа данных для моделей линейной регрессии (службы Analysis Services — интеллектуальный анализ данных)](mining-model-content-for-linear-regression-models-analysis-services-data-mining.md).  
  
 Визуальное представление диаграммы можно скопировать в буфер обмена, а лежащие в ее основе данные и формулы — нет. Чтобы узнать формулу регрессии для линии, можно создать запрос к содержимому модели. Дополнительные сведения см. в разделе [Примеры запросов модели линейной регрессии](linear-regression-model-query-examples.md).  
  
## <a name="restrictions-on-scatter-plots"></a>Ограничения точечных диаграмм  
 Точечную диаграмму можно создать только в том случае, если модель, выбранная на вкладке **Выбор входных данных** , содержит непрерывный прогнозируемый атрибут. Другие параметры выбирать не нужно, тип точечной диаграммы автоматически отображается на вкладке **Диаграмма точности прогнозов** на основе модели и типа атрибута.  
  
 Несмотря на то что модели временной последовательности предсказывают непрерывные числа, нельзя измерить точность модели временной последовательности с помощью точечной диаграммы. Для этого существуют другие методы, например выделение части исторических данных. Дополнительные сведения см. в разделе [Примеры запросов моделей временных рядов](time-series-model-query-examples.md).  
  
## <a name="related-content"></a>См. также  
 Следующие разделы содержат дополнительные сведения о том, как создавать и использовать точечные диаграммы и связанные точечные диаграммы.  
  
|Подраздел|Ссылки|  
|------------|-----------|  
|Объясняет, как создать диаграмму точности прогнозов для модели целевой рассылки.|[Учебник по основам интеллектуального анализа данных](../../tutorials/basic-data-mining-tutorial.md)<br /><br /> [Проверка точности при помощи диаграммы точности прогнозов &#40;учебник интеллектуального анализа данных&#41;](../../tutorials/testing-accuracy-with-lift-charts-basic-data-mining-tutorial.md)|  
|Объясняет типы соответствующих диаграмм.|[Диаграмма точности прогнозов &#40;службы Analysis Services — Интеллектуальный анализ данных&#41;](lift-chart-analysis-services-data-mining.md)<br /><br /> [Диаграмма роста прибыли &#40;службы Analysis Services — Интеллектуальный анализ данных&#41;](profit-chart-analysis-services-data-mining.md)<br /><br /> [Матрица классификации &#40;службы Analysis Services — Интеллектуальный анализ данных&#41;](classification-matrix-analysis-services-data-mining.md)|  
|Описывает использование перекрестной проверки для моделей интеллектуального анализа данных и структур интеллектуального анализа данных.|[Перекрестная проверка &#40;службы Analysis Services — Интеллектуальный анализ данных&#41;](cross-validation-analysis-services-data-mining.md)|  
|Описывает шаги для создания диаграммы точности прогнозов и других диаграмм точности.|[Тестирование и проверка задачи и инструкции по &#40;интеллектуального анализа данных&#41;](testing-and-validation-tasks-and-how-tos-data-mining.md)|  
  
## <a name="see-also"></a>См. также  
 [Тестирование и проверка &#40;интеллектуального анализа данных&#41;](testing-and-validation-data-mining.md)  
  
  
