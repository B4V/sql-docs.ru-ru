---
title: Создание фильтра трассировки (Transact-SQL) | Документация Майкрософт
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- database-engine
ms.topic: conceptual
helpviewer_keywords:
- filters [SQL Server], traces
- traces [SQL Server], filters
ms.assetid: 7b976a84-7381-43a6-a828-ba83ada71cbe
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: fed48fdb4b6e86bc2c1920e80ea9e62ba4b73a7b
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48177436"
---
# <a name="set-a-trace-filter-transact-sql"></a>создать фильтр трассировки (Transact-SQL)
  В этом разделе описывается, как использовать хранимые процедуры для создания фильтра, который возвращает только данные, необходимые для трассируемого события.  
  
### <a name="to-set-a-trace-filter"></a>Установка фильтра трассировки  
  
1.  Чтобы остановить трассировку, если она уже выполняется, выполните процедуру **sp_trace_setstatus** , указав параметр **@status =0**.  
  
2.  Выполните хранимую процедуру **sp_trace_setfilter** , чтобы определить тип данных, которые необходимо получить для трассируемого события.  
  
> [!IMPORTANT]  
>  Параметры всех хранимых процедур [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] (**sp_trace_* xx***), в отличие от обычных хранимых процедур, жестко типизированы и не поддерживают автоматическое преобразование типов данных. Если эти аргументы указываются с неправильными типами данных входных параметров, как указано в описании их аргументов, хранимая процедура возвратит ошибку.  
  
## <a name="see-also"></a>См. также  
 [Фильтрация трассировки](../../relational-databases/sql-trace/filter-a-trace.md)   
 [sp_trace_setfilter (Transact-SQL)](/sql/relational-databases/system-stored-procedures/sp-trace-setfilter-transact-sql)   
 [Хранимая процедура sp_trace_setstatus (Transact-SQL)](/sql/relational-databases/system-stored-procedures/sp-trace-setstatus-transact-sql)   
 [Системные хранимые процедуры (Transact-SQL)](/sql/relational-databases/system-stored-procedures/system-stored-procedures-transact-sql)   
 [Хранимые процедуры приложения SQL Server Profiler (Transact-SQL)](/sql/relational-databases/system-stored-procedures/sql-server-profiler-stored-procedures-transact-sql)  
  
  
