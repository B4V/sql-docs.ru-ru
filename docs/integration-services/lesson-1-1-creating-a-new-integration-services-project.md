---
title: Шаг 1. Создание нового проекта служб Integration Services | Документы Майкрософт
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: tutorial
ms.assetid: f14521b5-941e-443b-8f5e-385f98e37fbf
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 8d8fff1dbb0d7e44ad814c312be65efccaa731ab
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2018
ms.locfileid: "47792482"
---
# <a name="lesson-1-1---creating-a-new-integration-services-project"></a>Занятие 1–1. Создание проекта служб Integration Services
Первым шагом создания пакета в службах [!INCLUDE[ssISnoversion](../includes/ssisnoversion-md.md)] будет создание проекта служб [!INCLUDE[ssISnoversion](../includes/ssisnoversion-md.md)] . Этот проект содержит шаблоны для объектов (источников данных, представлений источников данных и пакетов), которые используются в решении преобразования данных.  
  
Пакеты, которые будут создаваться в этом учебнике по службам [!INCLUDE[ssISnoversion](../includes/ssisnoversion-md.md)] , преобразуют значения, зависящие от локаля и региональных стандартов. Если компьютер не настроен на использование регионального параметра «Английский (США)», необходимо установить дополнительные свойства в пакете. Пакеты, использовавшиеся на занятиях 2–5, скопированы из пакета, созданного на занятии 1, поэтому в скопированных пакетах не обязательно обновлять свойства, зависящие от языка и региональных стандартов.  
  
> [!NOTE]  
> Для выполнения упражнений этого учебника требуется Microsoft SQL Server Data Tools.  
>   
> Дополнительные сведения об установке SQL Server Data Tools см. в разделе [Загрузка SQL Server Data Tools](http://msdn.microsoft.com/data/hh297027).  
  
### <a name="to-create-a-new-integration-services-project"></a>Создание нового проекта служб Integration Services  
  
1.  В меню **Пуск** последовательно укажите пункты **Все программы**, **Microsoft SQL Server**и выберите **SQL Server Data Tools**.  
  
2.  В меню **Файл** укажите **Создать**и выберите пункт **Проект** , чтобы создать новый проект служб [!INCLUDE[ssISnoversion](../includes/ssisnoversion-md.md)] .  
  
3.  В диалоговом окне **Создать проект** разверните узел **Бизнес-аналитика** в категории **Установленные шаблоны**и выберите **Проект служб Integration Services** на панели **Шаблоны** .  
  
4.  В поле **Имя** измените заданное по умолчанию имя на **Учебник по службам SQL Server Integration Services**. При необходимости снимите флажок **Создать каталог для решения** .  
  
5.  Согласитесь с местоположением по умолчанию или нажмите кнопку **Обзор** , чтобы найти нужную папку. В диалоговом окне **Расположение проекта** щелкните папку и нажмите кнопку **Выбрать папку**.  
  
6.  Нажмите кнопку **ОК**.  
  
    По умолчанию будет создан пустой пакет с именем **Package.dtsx**и добавлен к проекту в узле «Пакеты служб SSIS».  
  
7.  На панели инструментов **обозревателя решений** щелкните правой кнопкой мыши файл **Package.dtsx**, выберите команду **Переименовать**и переименуйте пакет по умолчанию в **Урок 1.dtsx**.  
  
## <a name="next-task-in-lesson"></a>Следующая задача занятия  
[Шаг 2. Добавление и настройка диспетчера соединений с неструктурированными файлами](../integration-services/lesson-1-2-adding-and-configuring-a-flat-file-connection-manager.md)  
  
