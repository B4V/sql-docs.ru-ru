---
title: Задача "Проверка целостности базы данных" | Документы Майкрософт
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: conceptual
f1_keywords:
- sql13.dts.designer.checkdatabaseintegritytask.f1
helpviewer_keywords:
- data integrity [Integration Services]
- Check Database Integrity task [Integration Services]
- checking database consistency
- database consistency checks [Integration Services]
- verifying database consistency
- integrity checking [Integration Services]
ms.assetid: 5a82fe99-4503-429f-9337-e6bac7649fe4
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: a1ebe02d317656b0603b045f0cd048fe6779e32e
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2018
ms.locfileid: "47771562"
---
# <a name="check-database-integrity-task"></a>Задача «Проверка целостности базы данных»
  Задача «Проверка целостности базы данных» заключается в проверке распределения и структурной целостности всех объектов в заданной базе данных. Можно проверить одну или несколько баз данных. Кроме того, можно задать проверку индексов базы данных.  
  
 Задача проверки целостности базы данных содержит инструкцию DBCC CHECKDB. Дополнительные сведения см. в разделе [DBCC CHECKDB (Transact-SQL)](../../t-sql/database-console-commands/dbcc-checkdb-transact-sql.md).  
  
## <a name="configuration-of-the-check-database-integrity-task"></a>Настройка задачи «Проверка целостности базы данных»  
 Свойства задаются с помощью конструктора служб [!INCLUDE[ssIS](../../includes/ssis-md.md)] . Эта задача находится в разделе **Задачи плана обслуживания** **области элементов** в конструкторе служб [!INCLUDE[ssIS](../../includes/ssis-md.md)] .  
  
 Дополнительные сведения о свойствах, которые можно задать в конструкторе служб [!INCLUDE[ssIS](../../includes/ssis-md.md)] , см. в следующем разделе:  
  
-   [Задача "Проверка целостности базы данных" (план обслуживания)](../../relational-databases/maintenance-plans/check-database-integrity-task-maintenance-plan.md)  
  
 Дополнительные сведения об установке этих свойств в конструкторе служб [!INCLUDE[ssIS](../../includes/ssis-md.md)] см. в следующем разделе:  
  
-   [Задание свойств задач или контейнеров](http://msdn.microsoft.com/library/52d47ca4-fb8c-493d-8b2b-48bb269f859b)  
  
  
