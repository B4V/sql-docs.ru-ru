---
title: Microsoft ODBC Driver for SQL Server | Документация Майкрософт
ms.custom: ''
ms.date: 08/09/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
ms.assetid: 9f2ae91b-06af-4c9a-9d24-062df7bc4662
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 8fb8dd7b195ca94751eca51da36340ce201246d1
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MTE75
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2018
ms.locfileid: "47669232"
---
# <a name="microsoft-odbc-driver-for-sql-server"></a>Microsoft ODBC Driver for SQL Server

[!INCLUDE[Driver_ODBC_Download](../../includes/driver_odbc_download.md)]

ODBC — это основной собственный API доступа к данным для приложений, написанных на языках C и C++ для SQL Server. Имеется драйвер ODBC для большинства источников данных. Другие языки, которые могут использовать ODBC включают COBOL, Perl, PHP и Python. ODBC широко используется в сценариях интеграции данных.

Драйвер ODBC поставляется с такими средствами как [**sqlcmd**](../../tools/sqlcmd-utility.md) и [**bcp**](../../tools/bcp-utility.md). Служебная программа **sqlcmd** позволяет выполнять инструкции Transact-SQL, системные процедуры и сценарии SQL. Служебная программа **bcp** используется для массового копирования данных в нужном вам формате между экземпляром Microsoft SQL Server и файлом данных. Также можно использовать **bcp** для импорта большого количества новых строк в таблицы SQL Server или экспорта данных из таблиц в файлы данных.  

## <a name="code-example-in-c"></a>Пример кода в C++

В следующем примере C++ показано, как использовать интерфейсы API ODBC для подключения и доступа к базе данных.

- [Пример кода C++ с использованием ODBC](../../odbc/reference/sample-odbc-program.md)

## <a name="download"></a>Загрузить

- ![Загрузки стрелка вниз обведены](../../ssdt/media/download.png)[для загрузки драйвера ODBC](download-odbc-driver-for-sql-server.md)

## <a name="documentation"></a>Документация

### <a name="features"></a>Компоненты

- [Пользовательские поставщики хранилища ключей](../../connect/odbc/custom-keystore-providers.md)
- [Ключевые слова и атрибуты строки подключения и имени DSN](dsn-connection-string-attribute.md)
- [Собственный клиент SQL Server](../../relational-databases/native-client/features/sql-server-native-client-features.md) (функции, доступные также применяется, без OLEDB, драйвер ODBC для SQL Server)
- [Использование Always Encrypted](../../connect/odbc/using-always-encrypted-with-the-odbc-driver.md)
- [Использование Azure Active Directory](../../connect/odbc/using-azure-active-directory.md)
- [Использование разрешения IP-адресов прозрачной сети](../../connect/odbc/using-transparent-network-ip-resolution.md)

### <a name="linux-and-macos"></a>Linux и macOS

- [Установка драйвера](../../connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server.md)
- [Подключение к SQL Server](../../connect/odbc/linux-mac/connection-string-keywords-and-data-source-names-dsns.md)
- [Подключение с помощью **bcp**](../../connect/odbc/linux-mac/connecting-with-bcp.md)
- [Соединение с помощью **sqlcmd**](../../connect/odbc/linux-mac/connecting-with-sqlcmd.md)
- [Трассировка доступа к данным](../../connect/odbc/linux-mac/data-access-tracing-with-the-odbc-driver-on-linux.md)
- [Часто задаваемые вопросы](../../connect/odbc/linux-mac/frequently-asked-questions-faq-for-odbc-linux.md)
- [Установка диспетчера драйверов](../../connect/odbc/linux-mac/installing-the-driver-manager.md)
- [Известные проблемы](../../connect/odbc/linux-mac/known-issues-in-this-version-of-the-driver.md)
- [Указания по программированию](../../connect/odbc/linux-mac/programming-guidelines.md)
- [Заметки о выпуске](../../connect/odbc/linux-mac/release-notes.md)
- [Поддержка высокого уровня доступности и аварийного восстановления](../../connect/odbc/linux-mac/odbc-driver-on-linux-support-for-high-availability-disaster-recovery.md)
- [Использование встроенной проверки подлинности (Kerberos)](../../connect/odbc/linux-mac/using-integrated-authentication.md)

### <a name="windows"></a>Windows

- [Образец асинхронного выполнения (метод уведомления)](../../connect/odbc/windows/asynchronous-execution-notification-method-sample.md)
- [Устойчивость подключения в драйвере ODBC в Windows](../../connect/odbc/windows/connection-resiliency-in-the-windows-odbc-driver.md)
- [Организация пулов соединений с учетом драйвера](../../connect/odbc/windows/driver-aware-connection-pooling-in-the-odbc-driver-for-sql-server.md)
- [Функции и изменения в поведении](../../connect/odbc/windows/features-of-the-microsoft-odbc-driver-for-sql-server-on-windows.md)
- [Заметки о выпуске](../../connect/odbc/windows/release-notes.md)
- [Системные требования, установка и файлы драйвера](../../connect/odbc/windows/system-requirements-installation-and-driver-files.md)



## <a name="community"></a>Сообщество  
- [Блог команды разработчиков Microsoft ODBC Driver For SQL Server](http://blogs.msdn.com/sqlnativeclient/default.aspx)  
- [Форум по доступу к данным SQL Server](http://social.technet.microsoft.com/Forums/en/sqldataaccess/threads)  
