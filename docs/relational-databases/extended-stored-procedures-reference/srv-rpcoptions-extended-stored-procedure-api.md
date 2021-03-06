---
title: srv_rpcoptions (интерфейс API расширенных хранимых процедур) | Документы Майкрософт
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology:
- database-engine
ms.topic: reference
apiname:
- srv_rpcoptions
apilocation:
- opends60.dll
apitype: DLLExport
dev_langs:
- C++
helpviewer_keywords:
- srv_rpcoptions
ms.assetid: dbcce5d1-d5a1-4379-9597-04e43af5923d
author: rothja
ms.author: jroth
manager: craigg
ms.openlocfilehash: 266c08c4e19d3cf2f3b2daebe3b6ac43ae0ca75e
ms.sourcegitcommit: 110e5e09ab3f301c530c3f6363013239febf0ce5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2018
ms.locfileid: "48905064"
---
# <a name="srvrpcoptions-extended-stored-procedure-api"></a>srv_rpcoptions (API-интерфейс расширенных хранимых процедур)
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
    
> [!IMPORTANT]  
>  [!INCLUDE[ssNoteDepFutureDontUse](../../includes/ssnotedepfuturedontuse-md.md)] Используйте вместо этого интеграцию со средой CLR.  
  
 Возвращает параметры времени выполнения для текущей удаленной хранимой процедуры.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
  
DBUSMALLINT srv_rpcoptions ( SRV_PROC *  
srvproc   
);  
```  
  
## <a name="arguments"></a>Аргументы  
 *srvproc*  
 Указатель на структуру SRV_PROC, представляющую собой дескриптор соединения с клиентом (в данном случае — дескриптор, получивший удаленную хранимую процедуру). Эта структура содержит сведения, которые используются библиотекой API-интерфейса расширенных хранимых процедур для управления связью и передачи данных между приложением и клиентом.  
  
## <a name="returns"></a>Возвращает  
 Битовая карта, которая содержит флаги времени выполнения, соединенные логической операцией ИЛИ для текущей удаленной хранимой процедуры. При отсутствии текущей удаленной хранимой процедуры возвращается значение 0 и формируется сообщение.  
  
## <a name="remarks"></a>Remarks  
 В следующей таблице описывается каждый флаг времени выполнения.  
  
|Флаг времени выполнения|Описание|  
|--------------------|-----------------|  
|SRV_NOMETADATA|Клиент запросил результаты без метаданных. Этот флаг используется, только когда клиент связывается с экземпляром [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Приложение API-интерфейса расширенных хранимых процедур не может исключить метаданные.|  
|SRV_RECOMPILE|Клиент запросил повторную компиляцию удаленной хранимой процедуры перед ее выполнением. Этот флаг не может применяться к приложению API-интерфейса расширенных хранимых процедур.|  
  
> [!IMPORTANT]  
>  Необходимо тщательно просмотреть исходный код расширенных хранимых процедур и проверить скомпилированные библиотеки DLL перед их установкой на рабочий сервер. Сведения о проверке безопасности см. на следующем [веб-сайте Майкрософт](http://go.microsoft.com/fwlink/?LinkID=54761&amp;clcid=0x409http://msdn.microsoft.com/security/).  
  
  
