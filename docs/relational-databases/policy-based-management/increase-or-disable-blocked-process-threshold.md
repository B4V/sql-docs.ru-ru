---
title: Увеличение или отключение порога заблокированных процессов | Документация Майкрософт
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology:
- database-engine
ms.topic: conceptual
helpviewer_keywords:
- Best Practices [Database Engine]
ms.assetid: 71db8ef6-341b-4465-99db-5c63e48d4c7d
author: MikeRayMSFT
ms.author: mikeray
manager: craigg
ms.openlocfilehash: 523ac3bfe8f1b9f96840cbfe5ca523bf0640cf79
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2018
ms.locfileid: "47717852"
---
# <a name="increase-or-disable-blocked-process-threshold"></a>Увеличение или отключение порога заблокированных процессов
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  Это правило проверяет, имеет ли параметр «blocked process threshold» значение 0 (отключен) или значение, большее или равное 5 (секундам). Присвоение параметру «blocked process threshold» значения от 1 до 4 может привести к постоянной работе монитора взаимоблокировок. Эти значения следует использовать только для устранения неполадок. Их нельзя устанавливать на долгое время или в рабочей среде без участия представителей службы поддержки пользователей [!INCLUDE[msCoName](../../includes/msconame-md.md)] .  
  
## <a name="best-practices-recommendations"></a>Рекомендации  
 Чтобы решить эту проблему, присвойте параметру «blocked process threshold» значение 5 (секунд) или больше либо отключите порог блокировки процессов, присвоив этому параметру значение 0. Чтобы присвоить параметру «blocked process threshold» значение `5` секунд, выполните следующую инструкцию:  
  
```  
sp_configure 'show advanced options', 1 ;  
GO  
RECONFIGURE ;  
GO  
sp_configure 'blocked process threshold', 5 ;  
GO  
RECONFIGURE ;  
GO  
```  
  
## <a name="for-more-information"></a>Дополнительные сведения см. в разделе  
 [Параметр конфигурации сервера «blocked process threshold»](../../database-engine/configure-windows/blocked-process-threshold-server-configuration-option.md)  
  
## <a name="see-also"></a>См. также:  
 [Наблюдение с помощью управления на основе политик и принудительное применение рекомендаций с помощью управления на основе политик](../../relational-databases/policy-based-management/monitor-and-enforce-best-practices-by-using-policy-based-management.md)  
  
  
