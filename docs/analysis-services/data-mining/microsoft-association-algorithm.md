---
title: Алгоритм взаимосвязей Майкрософт | Документы Microsoft
ms.date: 05/08/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: data-mining
ms.topic: conceptual
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: c5a6f5046c93355b3b1359c59d2e935c9aa6288a
ms.sourcegitcommit: c12a7416d1996a3bcce3ebf4a3c9abe61b02fb9e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2018
ms.locfileid: "34017191"
---
# <a name="microsoft-association-algorithm"></a>Алгоритм взаимосвязей (Майкрософт)
[!INCLUDE[ssas-appliesto-sqlas](../../includes/ssas-appliesto-sqlas.md)]
  Алгоритм взаимосвязей [!INCLUDE[msCoName](../../includes/msconame-md.md)] часто используется для механизмов выработки рекомендаций. Механизм рекомендаций рекомендует продукты пользователям на основе элементов, которые они уже купили или к которым проявили интерес. Алгоритм взаимосвязей [!INCLUDE[msCoName](../../includes/msconame-md.md)] удобно использовать для анализа потребительской корзины.   
  
 Модели взаимосвязей построены на наборах данных, содержащих идентификаторы для отдельных вариантов и элементов этих вариантов. Группа элементов в варианте называется *набор элементов*. Модель взаимосвязей состоит из рядов наборов элементов и правил, описывающих, как эти элементы группируются в вариантах. Правила, определяемые алгоритмом, могут использоваться для прогнозирования вероятных будущих покупок покупателей на основе элементов, уже имеющихся в корзине покупателя. На следующей диаграмме представлен ряд правил в наборе элементов.  
  
 ![Набор правил для модели взаимосвязей](../../analysis-services/data-mining/media/association.gif "набор правил для модели взаимосвязей")  
  
 Как видно на схеме, алгоритм взаимосвязей [!INCLUDE[msCoName](../../includes/msconame-md.md)] потенциально может находить множество правил внутри набора данных. Для описания набора элементов и формируемых ими правил алгоритм использует два параметра: мощность несущего множества и вероятность. Например, если X и Y представляют два элемента, которые могут находиться в корзине для покупок, то параметр несущего множества будет равен количеству вариантов в наборе данных, содержащих сочетание элементов X и Y. Используя параметр несущего множества в сочетании с пользовательскими параметрами *MINIMUM_SUPPORT* и *MAXIMUM_SUPPORT* , алгоритм управляет количеством создаваемых наборов элементов. Параметр вероятности, называемый также *достоверностью*, представляет часть вариантов в наборе данных, содержащих X и Y. Используя параметр вероятности в сочетании с параметром *MINIMUM_PROBABILITY* , этот алгоритм управляет количеством сформированных правил.  
  
## <a name="example"></a>Пример  
 Компания [!INCLUDE[ssSampleDBCoShort](../../includes/sssampledbcoshort-md.md)] изменяет функциональные возможности своего веб-сайта. Цель этого изменения заключается в увеличении успешных продаж продукции. Записи организации о каждой продаже хранятся в транзакционной базе данных, поэтому можно использовать алгоритм взаимосвязей [!INCLUDE[msCoName](../../includes/msconame-md.md)] для определения набора продуктов, которые часто покупаются вместе. Затем на основе продуктов, имеющихся в корзине клиентов, можно прогнозировать дополнительные продукты, в которых могут быть заинтересованы эти клиенты.  
  
## <a name="how-the-algorithm-works"></a>Принцип работы алгоритма  
 Алгоритм взаимосвязей [!INCLUDE[msCoName](../../includes/msconame-md.md)] просматривает набор данных для поиска элементов, которые находятся в варианте совместно. Затем алгоритм группирует в наборы элементов любые связанные элементы, найденные, как минимум, в количестве вариантов, определенных параметром *MINIMUM_SUPPORT* . Например, возможен набор элементов «Горный 200=Существующий, Спортивный 100=Существующий», поддержка которого может составлять 710. Затем алгоритм формирует правила из наборов элементов. Правила используются для прогнозирования наличия элемента в базе данных на основе наличия других определенных элементов, которые алгоритм определяет как значимые. Например, возможно правило «если Туристический 1000=существующий и Контейнер для фляги=существующий, то Фляга=существующий» с вероятностью 0,812. В этом примере алгоритм определяет, что если в корзине имеется туристическая шина 1000 и контейнер для фляги, то, вероятно, там может быть и фляга для воды.  
  
 Более подробное описание алгоритма, наряду со списком параметров для настройки поведения алгоритма и контроля над результатами в модели интеллектуального анализа данных, см. в разделе [Технический справочник по алгоритму взаимосвязей (Майкрософт)](../../analysis-services/data-mining/microsoft-association-algorithm-technical-reference.md).  
  
## <a name="data-required-for-association-models"></a>Данные, необходимые для моделей взаимосвязей  
 При подготовке данных для использования в модели правил взаимосвязей, необходимо учитывать требования к конкретному алгоритму, включая то, сколько данных для него требуется и как эти данные используются.  
  
 Требования к модели правил взаимосвязей являются следующими.  
  
-   **Единичный ключевой столбец** Каждая модель должна содержать один числовой или текстовый столбец, который уникальным образом определяет каждую запись. Составные ключи не допускаются.  
  
-   **Единственный прогнозируемый столбец** .   Модель взаимосвязей может иметь только один прогнозируемый столбец. Как правило, он представляет собой ключевой столбец вложенной таблицы, такой как перечень приобретенных продуктов. Эти значения должны быть дискретными или дискретизированными.  
  
-   **Входные столбцы** . Входные столбцы должны быть дискретными. Входные данные для модели взаимосвязей часто содержатся в двух таблицах. Например, в одной таблице могут содержаться сведения о клиенте, а в другой — сведения о покупках клиента. Можно ввести эти данные в модель с помощью вложенной таблицы. Дополнительные сведения о вложенных таблицах см. в разделе [Вложенные таблицы (службы Analysis Services — интеллектуальный анализ данных)](../../analysis-services/data-mining/nested-tables-analysis-services-data-mining.md).  
  
 Дополнительные сведения о типах содержимого и типах данных, поддерживаемых моделями взаимосвязей, см. в подразделе "Требования" раздела [Технический справочник по алгоритму взаимосвязей (Майкрософт)](../../analysis-services/data-mining/microsoft-association-algorithm-technical-reference.md).  
  
## <a name="viewing-an-association-model"></a>Просмотр модели взаимосвязей  
 Чтобы исследовать модель, можно использовать **Средство просмотра взаимосвязей (Майкрософт)**. При просмотре модели взаимосвязей в службах [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] представлены корреляции под различными углами зрения, что позволяет лучше понять связи и правила, обнаруживаемые в данных. На панели **Набор элементов** средства просмотра предоставлена подробная классификация наиболее часто встречающихся сочетаний или наборов элементов. На панели **Правила** представлен список правил, которые были выведены на основании данных, дополнительно приведены результаты вычисления вероятностей, а сами правила ранжированы по относительной важности. Средство просмотра сети зависимостей позволяет исследовать визуально, как связаны отдельные элементы. Дополнительные сведения см. в разделе [Просмотр модели с помощью средства просмотра кластеров (Майкрософт)](../../analysis-services/data-mining/browse-a-model-using-the-microsoft-cluster-viewer.md).  
  
 Более подробные сведения о любом из наборов элементов и правил можно найти, открыв модель в [средстве просмотра деревьев содержимого общего вида (Майкрософт)](../../analysis-services/data-mining/browse-a-model-using-the-microsoft-generic-content-tree-viewer.md). С моделью связано хранимое содержимое, которое включает несущее множество для каждого набора элементов, оценку для каждого правила и другие статистические данные. Дополнительные сведения см. в разделе [Mining Model Content for Association Models &#40;Analysis Services - Data Mining&#41;](../../analysis-services/data-mining/mining-model-content-for-association-models-analysis-services-data-mining.md).  
  
## <a name="creating-predictions"></a>Создание прогнозов  
 После обработки модели полученные правила и наборы элементов можно использовать для прогнозов. Прогнозы, выполняемые с помощью модели взаимосвязей, позволяют определить, какой элемент, скорее всего, обнаружится, если имеются сведения о присутствии указанного элемента, а сам прогноз может включать такую информацию, как вероятность, несущее множество или важность. Примеры создания запросов применительно к модели взаимосвязей см. в разделе [Примеры запросов моделей взаимосвязей](../../analysis-services/data-mining/association-model-query-examples.md).  
  
 Дополнительные сведения о создании запроса к модели интеллектуального анализа данных см. в разделе [Запросы интеллектуального анализа данных](../../analysis-services/data-mining/data-mining-queries.md).  
  
## <a name="performance"></a>Производительность  
 Процесс создания наборов элементов и расчета значений корреляции может потребовать много времени. Хотя в алгоритме правил взаимосвязей [!INCLUDE[msCoName](../../includes/msconame-md.md)] используются методы оптимизации для экономии памяти и ускорения обработки, следует знать, что могут возникнуть проблемы производительности, в частности, при следующих условиях:  
  
-   Применяется крупный набор данных, состоящий из большого количества отдельных элементов.  
  
-   Задано слишком маленькое значение минимального размера набора элементов.  
  
 Чтобы свести к минимуму время обработки и уменьшить сложность наборов элементов, можно попытаться сгруппировать связанные элементы по категориям перед выполнением анализа данных.  
  
## <a name="remarks"></a>Замечания  
  
-   Не поддерживается использование языка разметки прогнозирующих моделей (PMML) для создания моделей интеллектуального анализа данных.  
  
-   Поддерживается детализация.  
  
-   Поддерживается использование моделей интеллектуального анализа OLAP.  
  
-   Поддерживается создание измерений интеллектуального анализа данных.  
  
## <a name="see-also"></a>См. также  
 [Алгоритмы интеллектуального анализа данных & #40; Службы Analysis Services — Интеллектуальный анализ данных & #41;](../../analysis-services/data-mining/data-mining-algorithms-analysis-services-data-mining.md)   
 [Просмотр модели с помощью средства просмотра правил взаимосвязи (Microsoft)](../../analysis-services/data-mining/browse-a-model-using-the-microsoft-association-rules-viewer.md)   
 [Содержимое модели интеллектуального анализа данных для моделей взаимосвязей & #40; Службы Analysis Services — Интеллектуальный анализ данных & #41;](../../analysis-services/data-mining/mining-model-content-for-association-models-analysis-services-data-mining.md)   
 [Технический справочник по алгоритму взаимосвязей (Майкрософт)](../../analysis-services/data-mining/microsoft-association-algorithm-technical-reference.md)   
 [Примеры запросов к модели взаимосвязей](../../analysis-services/data-mining/association-model-query-examples.md)  
  
  
