---
title: MSSQLSERVER_1205 | Документация Майкрософт
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: supportability
ms.topic: conceptual
helpviewer_keywords:
- 1205 (Database Engine error)
ms.assetid: 9fe3f67c-df3c-4642-a3a4-ccc0e138b632
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: ef8a59c98bc6669a13b5a4ffeb516b4063db23c7
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2018
ms.locfileid: "48092184"
---
# <a name="mssqlserver1205"></a>MSSQLSERVER_1205
    
## <a name="details"></a>Сведения  
  
|||  
|-|-|  
|Название продукта|SQL Server|  
|Идентификатор события|1205|  
|Источник события|MSSQLSERVER|  
|Компонент|SQLEngine|  
|Символическое имя|LK_VICTIM|  
|Текст сообщения|Транзакция (с идентификатором процесса %d) вызвала взаимоблокировку ресурсов %.*ls с другим процессом и была выбрана в качестве жертвы для ее разрешения. Запустите транзакцию повторно.|  
  
## <a name="explanation"></a>Объяснение  
 Доступ к ресурсам осуществляется отдельными транзакциями в конфликтном порядке, что приводит к взаимоблокировке. Пример:  
  
-   Транзакция1 обновляет строку **Таблица1.Строка1**, а транзакция2 в то же время обновляет строку **Таблица2.Строка2**.  
  
-   Транзакция1 пытается произвести обновление строки **Таблица2.Строка2**, но происходит блокировка, так как транзакция2 еще не зафиксирована.  
  
-   Теперь транзакция2 пытается провести обновление строки **Таблица1.Строка1**, но происходит блокировка, так как транзакция1 еще не зафиксирована.  
  
-   Взаимоблокировка происходит из-за того, что транзакция1 ожидает завершения транзакции2, а транзакция2 ожидает завершения транзакции1.  
  
 Система обнаруживает эту взаимоблокировку и выбирает одну из транзакций в качестве жертвы взаимоблокировки, публикуя данное сообщение и производя откат транзакции-жертвы.  
  
## <a name="user-action"></a>Действие пользователя  
 Выполните транзакцию еще раз. Во избежание взаимоблокировок можно изменить выполняемое приложение. Выбранную «жертвой» транзакцию можно выполнить повторно, вероятность ее успешного выполнения высока и зависит от того, какие операции выполнялись одновременно.  
  
 Для предотвращения взаимоблокировок можно сделать так, чтобы транзакции обращались к строкам в одном и том же порядке (**Table1**, затем **Table2**). При таком подходе могут возникнуть блокировки, но не взаимоблокировка.  
  
  
