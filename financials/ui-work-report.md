---
title: "Планирование запуска отчета в определенную дату и время | Microsoft Docs"
description: "Узнайте о вводе отчета в очередь заданий и планирование его обработки в конкретные дату и время."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 16c9c8c896e3517f08a7326eef88ebc646834b1a
ms.contentlocale: ru-ru
ms.lasthandoff: 11/10/2017

---
# <a name="working-with-reports"></a>Работа с отчетами
Отчет собирает информацию на основе указанного набора критериев и организует и представляет информацию в удобном для восприятия и печати формате. Предусмотрено много отчетов, к которым можно получить доступ с помощью приложения. Отчеты обычно содержат сведения относительно контекста страницы, на которой вы находитесь. Например, страница **Клиент** включает отчеты для 10 лучших клиентов, статистику продаж и т. п.

Отчеты можно найти на вкладке **Отчет** на выбранных страницах или можно воспользоваться поиском для поиска по названию отчета. При открытии отчета отображается страница, позволяющая указать информацию (параметры и фильтры), которая определяет, что требуется включить в отчет. Например, в зависимости от отчета, можно указать интервал дат, определенную запись, такую как клиент, или порядок сортировки. Пример:

![Параметры отчета](media/report_options.png "Параметры отчета")

## <a name="previewing-a-report"></a>Предварительный просмотр отчета
Выберите **Просмотр**, чтобы посмотреть отчет в веб-браузере. Укажите на область отчета, чтобы появилась строка меню.  

![Панель инструментов предварительного просмотра отчета](media/report_viewer.png "Панель инструментов предварительного просмотра отчета")

Используйте строку меню для следующих целей:

-   Переход по страницам
-   Увеличение и уменьшение
-   Изменение размеров по размеру окна
-   Выберите текст

    Можно копировать текст из отчетов, а затем вставлять его в другие места, например на страницу в [!INCLUDE[d365fin](includes/d365fin_md.md)] или в Microsoft Word.  Например, при использовании мыши нажмите и удерживайте кнопку мыши в месте, с которого нужно начать, затем выберите одно или несколько слов, предложений или абзацев, перемещая мышь. Затем можно нажать правую кнопку мыши и выбрать команду **Копировать**. Выбранный текст можно вставить в любом требуемом месте.
-   Сдвиньте документ

    Можно переместить видимую область отчета в любом направлении, чтобы просмотреть другие области отчета. Это удобно, если отчет был увеличен для просмотра подробных сведений.  Например, при использовании мыши, нажмите и удерживайте клавишу мыши в любом месте предварительного просмотра отчета и перемещайте мышь.

-   Загрузка в PDF-файл на компьютере или в сети.
-   Печать


## <a name="saving-a-report"></a>Сохранение отчета
Можно сохранить отчет в PDF-документ, документ Microsoft Word или документ Microsoft Excel, выбрав пункт **Отправить**, затем выбрав нужный вариант.

## <a name="ScheduleReport"></a> Планирование выполнения отчета
Можно спланировать выполнение отчета в заданную дату и время. Спланированные отчеты вводятся в очередь заданий и обрабатываются в намеченное время, как и другие задания. Можно Сохранить обработанный отчет в файле, например Excel, Word или PDF, напечатать его на выбранном принтере или только обработать отчет. Если выбрано сохранить отчет в файл, обработанный отчет отправляется в область **Входящие отчеты** на домашней странице, где его можно просмотреть.

Можно планировать отчет при открытии отчета. Выберите действие **Планировать**, после чего введите сведения, такие как принтер, время и дата. Отчет добавляется в очередь заданий и будет выполнен в указанное время. Если отчет обработан, элемент будет удален из очереди заданий. Если обработанный отчет сохранен в файле, он будет доступен в области **Входящие отчеты**.

## <a name="PrintReport"></a>Печать отчета
Отчет можно напечатать с помощью кнопки **Печать** на странице параметров, которая появляется при открытии отчета, или из строки меню в режиме предварительного просмотра.

## <a name="using-saved-settings"></a>Использование сохраненных параметров
Отчет может содержать одну или несколько операций в поле **Сохраненные параметры**. *Сохраненные параметры* по существу представляют собой предопределенную группу параметров и фильтров, которые можно применить к отчету перед предварительным просмотром или отправкой отчета в файл. Сохраненные настройки обеспечивают быстрый и удобный способ последовательного создания отчетов, содержащих правильные данные.

Всегда доступны сохраненные настройки под названием **Последние использованные параметры и фильтры**. Этот пункт задает в отчете использование параметров и фильтров, которые использовались при последнем просмотре отчета.

>[!NOTE]
>Как администратор, вы можете создавать и управлять сохраненными параметрами для отчетов для всех пользователей. Дополнительные сведения см. в разделе [Управление сохраненными настройками в отчетах](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Изменение макета и вида отчета
Макет отчета определяет, что отображается в отчете, как он скомпонован и в каком стиле. Если требуется переключиться на другой макет, см. раздел [Практическое руководство. Смена макета, используемого для отчета](ui-how-change-layout-currently-used-report.md). Если требуется настроить собственный макет отчета, см. раздел [Практическое руководство. Создание и изменение пользовательского макета отчета](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>См. также
[Выбор принтера для отчета](ui-specify-printer-selection-reports.md)  
[Управление макетами отчетов и документов](ui-manage-report-layouts.md)  
[Работа с [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)
