---
title: MSSQL_ENG014121 | Документация Майкрософт
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- replication
ms.topic: conceptual
helpviewer_keywords:
- MSSQL_ENG014121 error
ms.assetid: c8595854-cce1-4566-ad64-d565555caded
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: c91d4a8739544f2fd2b516e60cacf2de1176c79d
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48077594"
---
# <a name="mssqleng014121"></a>MSSQL_ENG014121
    
## <a name="message-details"></a>Сведения о сообщении  
  
|||  
|-|-|  
|Название продукта|SQL Server|  
|Идентификатор события|14121|  
|Источник события|MSSQLSERVER|  
|Компонент|[!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)]|  
|Символическое имя||  
|Текст сообщения|Не удалось удалить распространитель "%s". С этим распространителем связаны базы данных распространителя.|  
  
## <a name="explanation"></a>Объяснение  
 Экземпляр [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] , настроенный как распространитель, не может быть удален из роли распространителя, т. к. имеются базы данных распространителя, связанные с этим экземпляром. Эта ошибка возникает при попытке удалить базу данных распространителя, связанную с одним или несколькими издателями.  
  
## <a name="user-action"></a>Действие пользователя  
 Чтобы найти имена издателей и баз данных, связанных с конкретным распространителем, выполните хранимую процедуру [sp_helpdistpublisher &#40;Transact-SQL&#41;](/sql/relational-databases/system-stored-procedures/sp-helpdistpublisher-transact-sql) из любой базы данных в этом распространителе.  
  
 Выполните хранимую процедуру [sp_dropdistributiondb &#40;Transact-SQL&#41;](/sql/relational-databases/system-stored-procedures/sp-dropdistributiondb-transact-sql) для всех баз данных, связанных с этим распространителем. После того, как будут удалены все связи баз данных распространителя, распространение можно будет отключить.  
  
## <a name="see-also"></a>См. также  
 [Справочник по ошибкам и событиям (репликация)](errors-and-events-reference-replication.md)   
 [Настройка распространения](configure-distribution.md)  
  
  
