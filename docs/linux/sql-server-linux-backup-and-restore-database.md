---
title: "Резервное копирование и восстановление баз данных SQL Server в Linux | Документы Microsoft"
description: "Узнайте, как резервное копирование и восстановление баз данных SQL Server в Linux."
author: MikeRayMSFT
ms.author: mikeray
manager: jhubbard
ms.date: 03/17/2017
ms.topic: article
ms.prod: sql-linux
ms.technology: database-engine
ms.assetid: d30090fb-889f-466e-b793-5f284fccc4e6
ms.translationtype: MT
ms.sourcegitcommit: ea75391663eb4d509c10fb785fcf321558ff0b6e
ms.openlocfilehash: 6bd05a89f0c06bc03de931b898be18f3cbea0c8c
ms.contentlocale: ru-ru
ms.lasthandoff: 08/02/2017

---
# <a name="backup-and-restore-sql-server-databases-on-linux"></a>Резервное копирование и восстановление баз данных SQL Server в Linux

[!INCLUDE[tsql-appliesto-sslinux-only](../includes/tsql-appliesto-sslinux-only.md)]

Резервные копии баз данных может занять от RC2 2017 г. SQL Server в Linux с помощью тех же средств, как другие платформы. На сервере Linux, можно использовать `sqlcmd` для подключения к SQL Server и создания резервных копий. В операционной системе Windows можно подключиться к SQL Server в Linux и резервных копий с помощью пользовательского интерфейса. Функциональные возможности резервного копирования является одинаковым для платформы. Например, можно сделать резервную копию баз данных локально, чтобы удаленные диски, а также к [службы хранилища больших двоичных объектов Microsoft Azure](http://msdn.microsoft.com/library/dn435916.aspx). 

## <a name="backup-with-sqlcmd"></a>Резервное копирование с помощью sqlcmd

В следующем примере `sqlcmd` подключается к локальному экземпляру SQL Server и принимает полной резервной копии пользовательской базы данных называется `demodb`.

```bash
sqlcmd -H localhost -U SA -Q "BACKUP DATABASE [demodb] TO DISK = N'var/opt/mssql/data/demodb.bak' WITH NOFORMAT, NOINIT, NAME = 'demodb-full', SKIP, NOREWIND, NOUNLOAD, STATS = 10"
```

При выполнении команды SQL Server предложит ввести пароль. После ввода пароля оболочки возвратит результаты работы резервного копирования. Например:

```
Password:
10 percent processed.
21 percent processed.
32 percent processed.
40 percent processed.
51 percent processed.
61 percent processed.
72 percent processed.
80 percent processed.
91 percent processed.
Processed 296 pages for database 'demodb', file 'demodb' on file 1.
100 percent processed.
Processed 2 pages for database 'demodb', file 'demodb_log' on file 1.
BACKUP DATABASE successfully processed 298 pages in 0.064 seconds (36.376 MB/sec).
```

### <a name="backup-log-with-sqlcmd"></a>Журнал резервного копирования с помощью sqlcmd

В следующем примере `sqlcmd` подключается к локальному экземпляру SQL Server и принимает резервной копии заключительного фрагмента журнала. После завершения резервного копирования заключительного фрагмента журнала, база данных будет находиться в состоянии восстановления. 

```bash
sqlcmd -H localhost -U SA -Q "BACKUP LOG [demodb] TO  DISK = N'var/opt/mssql/data/demodb_LogBackup_2016-11-14_18-09-53.bak' WITH NOFORMAT, NOINIT,  NAME = N'demodb_LogBackup_2016-11-14_18-09-53', NOSKIP, NOREWIND, NOUNLOAD,  NORECOVERY ,  STATS = 5"
```


## <a name="restore-with-sqlcmd"></a>Восстановление с помощью sqlcmd

В следующем примере `sqlcmd` подключается к локальному экземпляру SQL Server и восстанавливает базу данных.

```bash
sqlcmd -H localhost -U SA -Q "RESTORE DATABASE [demodb] FROM  DISK = N'var/opt/mssql/data/demodb.bak' WITH  FILE = 1,  NOUNLOAD,  REPLACE,  STATS = 5"
```

## <a name="backup-and-restore-with-sql-server-management-studio-ssms"></a>Резервное копирование и восстановление с помощью SQL Server Management Studio (SSMS)

Среда SSMS с компьютера Windows можно использовать для подключения к базе данных Linux и резервное копирование через пользовательский интерфейс. 

>[!NOTE] 
> Используйте последнюю версию SSMS для подключения к SQL Server. Чтобы загрузить и установить последнюю версию, в разделе [загрузки SSMS](http://msdn.microsoft.com/library/mt238290.aspx). 

Ниже приведены шаги Создание резервной копии с помощью SSMS. 

1. Запустите SSMS и подключитесь к серверу в RC2 2017 г. SQL Server в Linux.

1. В обозревателе объектов щелкните правой кнопкой базу данных, нажмите кнопку **задачи**, а затем нажмите кнопку **создайте резервную копию...** .

1. В **резервное копирование копии базы данных** диалогового окна, проверьте параметры и параметры и нажмите кнопку **ОК**.
 
SQL Server завершает резервной копии базы данных.

Дополнительные сведения см. в разделе [используйте SSMS для управления SQL Server в Linux](sql-server-linux-manage-ssms.md).

### <a name="restore-with-sql-server-management-studio-ssms"></a>Восстановление с SQL Server Management Studio (SSMS) 

Следующие шаги описывают восстановление базы данных с помощью SSMS.

1. В среде SSMS щелкните правой кнопкой мыши **баз данных** и нажмите кнопку **восстановление баз данных...** . 

1. В разделе **источника** щелкните **устройства:** и нажмите кнопку с многоточием (...).

1. Найдите файл резервной копии базы данных и нажмите кнопку **ОК**. 

1. В разделе **план восстановления**, проверьте файл резервной копии и параметры. Нажмите кнопку **ОК**. 

1. SQL Server восстанавливает базу данных. 

## <a name="see-also"></a>См. также:

* [Создание полной резервной копии (SQL Server)](http://msdn.microsoft.com/library/ms187510.aspx)
* [Резервное копирование журнала транзакций (SQL Server)](http://msdn.microsoft.com/library/ms179478.aspx)
* [BACKUP (Transact-SQL)](http://msdn.microsoft.com/library/ms186865.aspx)
* [Резервное копирование в SQL Server по URL-адресу](http://msdn.microsoft.com/library/dn435916.aspx)
