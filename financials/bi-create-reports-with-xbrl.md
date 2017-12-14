---
title: "Практическое руководство. Создание отчетов с XBRL | Microsoft Docs"
description: "XBRL расшифровывается как eXtensible Business Reporting Language — расширяемый язык бизнес-отчетности. Это основанный на XML язык для разметки финансовых данных, помогающий эффективно и точно их обрабатывать, а также совместно их использовать."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: de7cf91736fd97943604237cee7093017e7c01f9
ms.contentlocale: ru-ru
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-reports-with-xbrl"></a>Практическое руководство. Создание отчетов с XBRL
XBRL расшифровывается как eXtensible Business Reporting Language — расширяемый язык бизнес-отчетности. Это основанный на XML язык для разметки финансовых данных, помогающий эффективно и точно их обрабатывать, а также совместно их использовать. Инициатива XBRL позволяет множеству компаний, занимающихся разработкой программного обеспечения для управления ресурсами предприятия, и международным бухгалтерским организациям создавать глобальную финансовую отчетность. Цель инициативы — создать стандарт для унификации учета финансовой информации для банков, инвесторов и государственных организаций. Такая отчетность может включать:  

 • финансовые отчеты;  
 • финансовая информация;  
 • нефинансовая информация;  
 • обязательная отчетность, такая как годовые и квартальные финансовые отчеты.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] позволяет организациям работать с данными в формате XBRL, а также использовать предоставляемые преимущества гибкости и автоматизации в отношении сбора и совместного использования данных.  

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language
XBRL (ра **с**ширяемый **я**зык **б**изнес-**о**тчетности) — это язык на основе XML для подготовки финансовой отчетности. XBRL предоставляет стандарт унификации отчетности для всех пользователей цепочки снабжения финансовой информацией: государственных и частных организаций, профессионалов в области учета, регулирующих органов, аналитиков, инвестиционного сообщества, рынков капитала, кредиторов, а также для ключевых третьих сторон, например разработчиков программного обеспечения и организаций, занимающихся сбором и упорядочением информации.  

Таксономии расположены на www.xbrl.org. Детальную информацию о таксономиях можно найти на сайте XBRL, откуда ее можно либо скачать, либо прочесть.  

Желающие получить финансовую информацию, предоставляют таксономию (документ XML), содержащую одну или более схем, каждая из которых содержит одну или большее количество строк, которые необходимо заполнить. Строки соответствуют отдельным финансовым позициям, которые требуются получателю информации. Необходимо импортировать таксономию в программу и затем заполнить схему (схемы), указывая, какой счет или счета соответствуют каждой строке, какой используется тип временного интервала, например оборот или баланс на дату. В некоторых случаях можно указать постоянную величину, например количество сотрудников. Теперь можно отправить заполненный документ (документ XML) лицу, запросившему информацию. Идея состоит в том, что такие действия могут повторяться, поэтому, при повторяющихся запросах, если в таксономии не было сделано никаких изменений, можно просто экспортировать новый заполненный документ для нового временного интервала.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>XBRL состоит из следующих компонентов  
**Спецификация** XBRL объясняет, что такое XBRL, как строить документы и таксономии XBRL. Спецификация XBRL содержит описание языка XBRL с технической точки зрения и рассчитана на технических специалистов.  

**Схемы** XBRL это низкоуровневые компоненты XBRL. Схемы — это физические файлы XSD, в которых заложено построение документов и таксономий.  

**Базы ссылок** XBRL это физические файлы XML, содержащие разнообразную информацию об элементах, определенных в Схемах XBRL, например, о метках для одного или нескольких языков, об их взаимосвязи, правилах суммирования элементов и т.д.  

XBRL **таксономия** это “словарь”, созданный группой, удовлетворяющий спецификации XBRL, и предназначенный для обмена бизнес-информацией.  

XBRL **документ** это бизнес-отчет, например финансовая отчетность, подготовленная в соответствии со спецификацией XBRL. Значения величин в документе объясняются в таксономии. Документ, это нечто бесполе зное, если неизвестна таксономия, на основе которой он подготовлен.  

## <a name="layered-taxonomies"></a>Послойные таксономии  
Таксономия может состоять из базовой, например, US GAAP или IAS, и одного или нескольких расширений. Чтобы отразить такую структуру, таксономия ссылается на одну или большее количество схем, каждая из которых представляет собой отдельную таксономию. Когда в базу данных загружаются дополнительные таксономии, новые элементы просто добавляются в конец существующих элементов.  

## <a name="linkbases"></a>Базы ссылок  
 В XBRL Спец. 2 таксономия описывается в нескольких файлах XML. Первичный файл XML — это собственно файл схемы таксономии (файл .xsd), содержащий неупорядоченный набор элементов или фактов, которые должны быть включены в отчет. Кроме того, с ним как правило связаны некоторые файлы баз ссылок (.xml). Файлы баз ссылок содержат данные, которые дополняют таксономию (файл .xsd). Существует шесть типов файлов баз ссылок, из которых четыре имеют отношение к XBRL "Имя продукта". Вот они:  

-   База ссылок меток: данная база ссылок содержит метки или названия элементов. Файл может содержать метки на разных языках, которые идентифицируются при помощи свойства XML, которое называется “Язык”. Идентификатор языка в рамках XML обычно содержит двухбуквенные аббревиатуры, и, хотя довольно просто догадаться, что означают эти аббревиатуры, никакой их связи с кодировкой языка в Windows, а также с кодировками языка, определенными для демонстрационных данных, не существует. Поэтому, когда пользователь просматривает языки для конкретной таксономии, он увидит все метки для первого элемента таксономии, т.е. он видит примеры для каждого языка. К таксономии может быть подключено несколько баз ссылок для меток, по одной базе для каждого языка.  

-   Представление базы ссылок: Данная база ссылок содержит информацию о структуре элементов, или точнее о том, как создатель таксономии предлагает программе представить таксономию пользователю. База ссылок содержит серии ссылок, каждая из которых связывает по два элемента, главный и подчиненный. Если применить все эти ссылки, элементы выстроятся в иерархическом порядке. Необходимо принять во внимание, что представление базы ссылок показывает: презентацию элементов пользователю.  

-   База ссылок расчетов: Данная база ссылок содержит информацию о том, как сворачиваются элементы. Структура данной базы аналогична структуре базы ссылок представлений, за исключением того, что каждая связь или так называемая «дуга» имеет такое свойство, как вес. Вес может быть равен либо 1, либо — 1, показывая, должен ли элемент прибавляться к своему главному элементу или вычитаться из него. Необходимо принимать во внимание, что свертывание в визуальном представлении не обязательно видно.  

-   Справочная база ссылок: Это база ссылок в файле xml, которая содержит дополнительную информацию о данных, требуемых создателем таксономии.

## <a name="to-set-up-xbrl-lines"></a>Настройка строк XBRL  
После импорта или обновления таксономии строки схем следует пополнить всей требуемой информацией. Эта информация включает в себя базовую информацию о организации, текущие финансовые отчеты, комментарии к финансовой отчетности, дополнительные таблицы, а также прочую информацию, необходимую для того, чтобы удовлетворить требования финансовой отчетности.  

Строки XBRL настраиваются путем задания соответствия между данным главной книги и данными таксономии.  

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Таксономии XBRL**, затем выберите связанную ссылку.  
2.  В окне **Таксономии XBRL** выберите таксономию из списка.  
3.  Выберите действие **Строки**.  
4.  Выберите строку и заполните поля.   
5.  Для получения дополнительной информации о том, что необходимо заполнять, выберите действие **Информация**.  
6.  Для настройки соответствия между счетами главной книги в плане счетов и строками XBLR выберите действие **Строки соответствия ГК**.  
7.  Для добавления комментариев к финансовым отчетам выберите действие **Заметки**.  

> [!NOTE]  
>  Можно производить экспорт только тех данных, которые соответствуют типу источника, выбранному в поле **Тип источника**, включая описание и примечания.  

> [!NOTE]  
>  Строки, которые неприменимы, могут быть помечены как тип строки **НЕ ПРИМЕНИМО**, и следовательно не будут экспортироваться.

 ## <a name="to-import-an-xbrl-taxonomy"></a>Импорт таксономии XBRL  
Первым шагом в работе с функциональностью XBRL должен быть импорт таксономии в базу данных организации. Таксономия состоит из одной или нескольких схем и некоторых баз ссылок. После завершения импорта схем и баз ссылок, а также после применения баз ссылок к схемам можно настроить строки и поставить в соответствие счетам Главной книги из плана счетов соответствующие строки таксономии.  

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Таксономии XBRL**, затем выберите связанную ссылку.  
2.  В окне **Таксономии XBRL** создайте новую строку и введите имя и описание таксономии.  
3.  Выберите действие **Схемы** и затем вставьте описание схемы.  
4.  Чтобы импортировать схему, в окне **XBRL Схемы** выберите действие **Импорт**, затем выберите папку и файл XSD. Нажмите кнопку **Открыть**.  
5.  Чтобы импортировать базу ссылок, в окне **XBRL Схемы** выберите действие **Базы ссылок**, затем выберите папку и файл XML. Нажмите кнопку **Открыть**.  
6.  Теперь можно применить базу ссылок к схеме. Повторите процедуру, пока все базы ссылок не будут импортированы.  
7. Выберите действие **Применить к таксономии**, чтобы применить базу ссылок к схеме.  

> [!IMPORTANT]  
>  Вместо применения баз ссылок по отдельности сразу после импорта можно дождаться, когда будут импортированы все базы ссылок, а затем применить их одновременно. Для этого нажмите кнопку **НЕТ** после отображения запроса на применение вновь импортированной базы ссылок к схеме. Затем выберите строки с базами ссылок, которые необходимо применить.  

## <a name="to-update-an-xbrl-taxonomy"></a>Обновление таксономии XBRL  
Когда производится изменение таксономии, необходимо обновить текущую таксономию. Причиной для обновления может быть изменение схемы, базы ссылок либо добавление новой базы ссылок. После обновления таксономии следует лишь настроить соответствие для изменившихся или новых строк.  

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Таксономии XBRL**, затем выберите связанную ссылку.  
2.  В окне **Таксономии XBRL** выберите действие **Схемы**.  
3.  Чтобы обновить схему, выберите схему, которую необходимо обновить, затем выберите действие **Импорт**.  
4.  Чтобы обновить или добавить новую базу ссылок, выберите действие **Базы ссылок**.  
5.  Выберите соответствующую базу ссылок или нажмите сочетание клавиш CTRL+N для вставки новой строки, выберите тип базы ссылок, а затем вставьте описание.  
6.  Для импорта базы ссылок выберите действие **Импорт**.  
7.  Нажмите кнопку **Да**, чтобы применить базу ссылок к схеме.  

## <a name="see-also"></a>См. также
[Финансы](finance.md)    
[Бизнес-аналитика](bi.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
