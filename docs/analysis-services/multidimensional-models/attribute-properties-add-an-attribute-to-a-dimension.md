---
title: "Добавление атрибута в измерение | Документы Microsoft"
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
- analysis-services/multidimensional-tabular
- analysis-services/data-mining
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- adding attributes
- automatic attribute creation
- attributes [Analysis Services], creating
- attributes [Analysis Services], adding
- manual attribute creation [Analysis Services]
ms.assetid: 25826ba1-2b38-4b34-bd3a-7eba116093ae
caps.latest.revision: 32
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 82e7f4e40a1c185b824f5533bff77c3ef917b535
ms.contentlocale: ru-ru
ms.lasthandoff: 09/01/2017

---
# <a name="attribute-properties---add-an--attribute-to-a-dimension"></a>Атрибут свойства — Добавление атрибута в измерение
  В службах [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)]добавлять атрибуты в измерение можно автоматически или вручную.  
  
 Чтобы создать атрибут автоматически, на вкладке **Структура измерения** конструктора измерений в среде [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)]выберите столбец, который нужно сопоставить с атрибутом, и перетащите его с панели **Представление источника данных** на панель **Атрибуты** . Служба создаст сопоставленный столбцу атрибут, которому будет присвоено имя столбца. Если атрибут с таким именем уже существует, службы [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] добавляют к имени порядковый номер, начинающийся с 1 для первого повторяющегося имени.  
  
 Чтобы создать атрибут вручную, выберите режим просмотра панели **Attributes** в виде сетки. В столбце имени в последней строке сетки щелкните  **\<новый атрибут >** элемента. Введите имя нового атрибута. Будет создан атрибут, не сопоставленный столбцу, а всем свойствам атрибута будут присвоены значения по умолчанию. Атрибут можно сопоставить столбцу в окне **Свойства** среды [!INCLUDE[ssBIDevStudio](../../includes/ssbidevstudio-md.md)] , настроив свойство **KeyColumns** нового атрибута.  
  
 Дополнительные сведения см. в разделах [Определение нового атрибута автоматически](../../analysis-services/multidimensional-models/attribute-properties-define-a-new-attribute-automatically.md), [Привязка атрибута к столбцу имени](../../analysis-services/multidimensional-models/attribute-properties-bind-an-attribute-to-a-name-column.md)и [Изменение свойства KeyColumn атрибута](../../analysis-services/multidimensional-models/attribute-properties-modify-the-keycolumn-property.md)добавлять атрибуты в измерение можно автоматически или вручную.  
  
## <a name="see-also"></a>См. также  
 [Справочник по свойствам атрибута измерения](../../analysis-services/multidimensional-models/dimension-attribute-properties-reference.md)  
  
  