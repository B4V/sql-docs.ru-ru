---
title: Настройка конструктора диаграмм баз данных (визуальные инструменты для баз данных) | Документация Майкрософт
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: ''
ms.topic: conceptual
f1_keywords:
- vdt.diagnostic.InstallSqlDiagramSupport
helpviewer_keywords:
- Database Diagram Designer
- database diagrams [SQL Server], Database Diagram Designer
- diagrams [SQL Server], Database Diagram Designer
ms.assetid: 927321ee-b459-4f5b-9719-4a7a95639143
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: 62add06b58d33af4f2e09ee02322a2cec5a9949b
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48108924"
---
# <a name="set-up-database-diagram-designer-visual-database-tools"></a>Настройка конструктора диаграмм баз данных (визуальные инструменты для баз данных)
  Чтобы можно было использовать конструктор диаграмм баз данных, его вначале должен установить член роли **db_owner** для контроля доступа к диаграммам.  
  
### <a name="to-set-up-database-diagramming"></a>Настройка создания схем баз данных  
  
1.  Разверните узел базы данных в обозревателе объектов.  
  
2.  В окне подключения к базе данных разверните узел «Диаграммы баз данных».  
  
3.  Нажмите кнопку **Да** , когда получите подсказку о необходимости настроить создание диаграмм баз данных.  
  
    > [!NOTE]  
    >  В базе данных [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] создаются таблица диаграмм базы данных, системные хранимые процедуры и системная функция.  
  
4.  Visual Studio создает следующие объекты в экземпляре [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]:  
  
    1.  таблица sysdiagrams;  
  
    2.  хранимая процедура sp_alterdiagram;  
  
    3.  хранимая процедура sp_creatediagram;  
  
    4.  хранимая процедура sp_dropdiagram;  
  
    5.  хранимая процедура sp_renamediagram;  
  
    6.  функция fn_diagramobjects;  
  
    7.  хранимая процедура sp_helpdiagrams;  
  
    8.  хранимая процедура sp_helpdiagramsdefinition;  
  
    9. хранимая процедура sp_upgraddiagrams.  
  
## <a name="see-also"></a>См. также  
 [Основные сведения о владении базы данных &#40;визуальных инструментах баз данных&#41;](visual-database-tools.md)   
 [Обновление диаграмм баз данных из предыдущих версий &#40;визуальных инструментах баз данных&#41;](upgrade-database-diagrams-from-previous-editions-visual-database-tools.md)   
 [ALTER AUTHORIZATION (Transact-SQL)](/sql/t-sql/statements/alter-authorization-transact-sql)  
  
  
