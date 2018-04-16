---
title: "Сведения о проектировании: основные понятия системы планирования | Microsoft Docs"
description: "Функции планирования содержатся в пакетном задании, которое сначала выбирает соответствующие товары и период планирования, а затем предлагает пользователю возможные действия, которые следует принять, на основе спроса/предложения и параметров планирования товаров."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e8eca3562639c864cb514b71c070d0fca4128d79
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Сведения о проектировании: основные понятия системы планирования
Функции планирования содержатся в пакетном задании, которое сначала выбирает соответствующие товары и период для планирования. Затем в соответствии с кодом нижнего уровня каждого товара (положением спецификации) пакетное задание вызывает модуль, вычисляющий план поставок путем балансировки наборов спрос-предложение и предлагая возможные действия пользователю. Предложенные действия отображаются как строки в журнале планирования или журнале заявок.  

![Журнал планирования](media/NAV_APP_supply_planning_1_planning_worksheet.png "NAV_APP_supply_planning_1_planning_worksheet")  

Планировщик компании, например закупщик или планировщик производства — это пользователь системы планирования. Система планирования помогает пользователю, выполняя объемные, но достаточно простые вычисления плана. Пользователь может сконцентрироваться на решении более сложных проблем, например обработке аномальных ситуаций.  

Работа системы планирования зависит от ожидаемого и фактического клиентского спроса, например прогнозов и заказов на продажу. При расчета плана программа предлагает пользователю специальные действия, связанные с возможной поставкой от поставщиков, сборочным или производственным участком либо перемещениями между складами. Предложенные действия могут быть создать новые заказы на поставку, например покупки или производственные заказы. Если заказы на поставку уже существуют, может быть предложено увеличение или ускорение выполнения заказов для удовлетворения изменений спроса.  

Еще одна цель системы планирования - не допустить увеличения объема складского хранения сверх необходимого предела. В случае уменьшения спроса система планирования предложит пользователю отложить, уменьшить количество или отменить существующие заказы на поставку.  

MPS и MRP, "Вычислить план оборота" и "Вычислить регенеративный план" — это функции одного модуля, содержащего логику планирования. Однако расчет плана поставки включает использование различных подсистем.  

Обратите внимание, что система планирования не включает отдельную логику для определения уровней производственных мощностей или точного планирования. Поэтому в этом случае планирование выполняется как отдельная дисциплина. Отсутствие прямой интеграции между двумя областями также означает, что существенные изменения производственной мощности или графика потребуют повторного планирования.  

## <a name="planning-parameters"></a>Параметры планирования  
Параметры планирования, заданные пользователем для товара или группы товаров, управляют тем, какие действия предложит система планирования в различных ситуациях. Параметры планирования определены на каждой карточке товара, чтобы контролировать время, количество и способ пополнения.  

Параметры планирования можно также указать для любой комбинации товара, варианта и склада, задав единицы хранения для каждой необходимой комбинации с последующим определением отдельных параметров.  

Дополнительные сведения см. в разделах [Сведения о проектировании: обработка политик дозаказа](design-details-handling-reordering-policies.md) и [Сведения о проектировании: параметры планирования](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Дата начала планирования  
Чтобы избежать плана поставок с открытыми заказами в прошлом, предлагающего потенциально невозможные действия, система планирования обрабатывает все даты до начальной даты планирования как замороженную зону, в которой действует следующее специальное правило.  

Весь спрос и поставки до даты начала периода планирования будут считаться частью запасов или будут считаться отгруженными.  

Иными словами, предполагается, что план для прошедшего периода выполнен в соответствии с данным планом.  

Дополнительные сведения см. в разделе [Сведения о проектировании: обработка заказов до даты начала планирования](design-details-dealing-with-orders-before-the-planning-starting-date.md).  

## <a name="dynamic-order-tracking-pegging"></a>Динамическая трассировка заказов (фиксация)  
Динамическая трассировка заказов создает сообщения о действиях в журнале планирования во время выполнения и не является частью системы планирования поставок в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Эта функция в реальном времени связывает спрос и количества, которыми этот спрос можно покрыть, всякий раз когда создается или меняется новый спрос или предложение.  

Например, если пользователь вводит или изменяет заказ на продажу, система динамической трассировки заказов сразу же выполняет поиск соответствующей поставки для удовлетворения спроса. Это может быть из запасов или ожидаемого заказа на поставку (заказ на покупку или производственный заказ). Если найден источник поставки, система создает звено между спросом и предложением, и источник отображается в доступном только для просмотра окне, доступ к которому осуществляется со строк задействованного документа. Если соответствующее предложение не удается найти, система динамического отслеживания заказов создает указания в журнале планирования, а предложения плана поставок отражают динамическое уравновешивание. Соответственно, динамическая система трассировки заказов предлагает очень простую систему планирования, которая может пригодиться планировщику и другим ролям во внутренней цепочке поставок.  

Соответственно, динамическую трассировку заказов можно рассматривать как средство, с помощью которого пользователь может решить, принимать ли предложения заказов на поставку. На стороне поставки пользователь может просмотреть, какой спрос привел к созданию поставки, а на стороне спроса — какая поставка должна удовлетворить спрос.  

![](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "NAV_APP_supply_planning_1_dynamic_order_tracking")  

Дополнительные сведения см. в разделе [Сведения о проектировании: резервирование, трассировка заказов и отправка сообщений о действиях](design-details-reservation-order-tracking-and-action-messaging.md).  

В организациях с низким потоком товаров и менее сложными структурами продуктов рекомендуется использовать динамическую трассировку заказов в качестве основного средства планирования поставок. Однако в более сложных средах система планирования должна использоваться для обеспечения должным образом сбалансированного плана поставок в любой момент времени.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Динамическая трассировка заказов и система планирования  
С первого взгляда может быть трудно найти отличия в системе планирования и динамической трассировке заказов. Обе эти функции отображают результат в журнале планирования, предлагая действия, которые должен предпринять планировщик. Однако, способ производства этого выхода отличается.  

Система планирования обрабатывает всю схему спроса и предложения товара на всех уровнях иерархии спецификации на временной шкале, в то время как динамическая трассировка заказов анализирует только ситуацию заказа, который ее активировал. При уравновешивании спроса и предложения система планирования создает ссылки в активируемом пользователем пакетном режиме, в то время как система динамического отслеживания заказов создает ссылки автоматически и сразу всякий раз, когда пользователь вводит спрос или предложение в программе, например заказ на продажу или заказ на покупку.  

Динамическая трассировка заказов позволяет устанавливать связь между спросом и поставкой при вводе данных на основе принципа "первым пришел — первым обслужен". Это может привести к нарушению приоритетности. Например, заказ на продажу, введенный первым, со сроком выполнения на следующий месяц можно связать с поставкой в запасах, в то время как следующий заказ на продажу со сроком выполнения на следующий день может привести к тому, что сообщение о действии создаст новый заказ на покупку для его выполнения, как показано на рисунке ниже.  

![](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "NAV_APP_supply_planning_1_dynamic_order_tracking_graph")  

В противоположность этому система планирования обрабатывает весь спрос и поставки для определенного товара в порядке приоритета в соответствии со сроками оплаты и типам заказа, то есть по принципу "первым требуется — первым обслужен" (FNFS). Она удаляет все связи трассировки заказа, которые были созданы динамически, и восстанавливает их в соответствии с приоритетом срока оплаты. Если система планирования запущена, это значит, что устранены все неравновесия между спросом и предложением, как показано ниже для одних и тех же данных.  

![](media/NAV_APP_supply_planning_1_planning_graph.png "NAV_APP_supply_planning_1_planning_graph")  

После выполнения планирования в таблице "Указание операции" не остается сообщений о действиях, поскольку они заменяются предлагаемыми действиями в журнале планирования.  

Дополнительные сведения см. в подразделе "Связи трассировки заказов во время планирования" раздела [Сведения о проектировании: балансировка поставки и спроса](design-details-balancing-supply-with-demand.md).  

## <a name="sequence-and-priority-in-planning"></a>Порядок и приоритет в планировании  
При составлении плана последовательность вычислений необходима для того, чтобы выполнить задание в разумное время. Кроме того, определение приоритетов требований и ресурсов играет важную роль в получении наиболее подходящих результатов.  

Система планирования в [!INCLUDE[d365fin](includes/d365fin_md.md)] управляется спросом. Высокоуровневые товары следует планировать до низкоуровневых, поскольку в плане для высокоуровневых товаров может быть создан дополнительный спрос для низкоуровневых товаров. Это означает, например, что розничные склады необходимо планировать до планирования центров распределения, поскольку план розничного склада может включать дополнительный спрос из центра распределения. На детальном уровне балансировки это также означает, что заказ на продажу не должен приводить к созданию нового заказа на поставку, если уже выпущенный заказ на поставку может удовлетворить заказ на продажу. Аналогично необходимо распределить поставку с определенным номером партии для удовлетворения общего спроса, если для удовлетворения другого спроса требуется эта определенная партия.  

### <a name="item-priority--low-level-code"></a>Приоритет/код нижнего уровня товара  
В производственной среде спрос на готовый продаваемый товар приведет к созданию производного спроса на компоненты, составляющие готовый товар. Структура спецификации определяет структуру компонентов и может охватывать несколько уровней полуфабрикатов. Планирование товара на одном уровне приведет к созданию производного спроса на компоненты на следующем уровне и так далее. В конечном итоге, это приведет к возникновению производного спроса для приобретенных товаров. Следовательно, система планирования планирует товары в порядке их рейтинга во всей иерархии спецификации, начиная с завершенных готовых к продаже товаров, расположенных вверху списка, и далее переходя по структуре продуктов к товарам низкого уровня (в соответствии с кодом нижнего уровня).  

![](media/NAV_APP_supply_planning_1_BOM_planning.png "NAV_APP_supply_planning_1_BOM_planning")  

Цифры показывают, в какой последовательности система делает предложения для заказов на поставку на верхнем уровне. Исходя из этого пользователь принимает предложения и для товаров более низкого уровня.  

Дополнительные сведения по вопросам производства см. в разделе [Сведения о проектировании: отправка профилей запасов](design-details-loading-the-inventory-profiles.md).  

### <a name="locations--transfer-level-priority"></a>Приоритет на уровне склада/перемещения  
Организациям, которые работают с несколькими складами, может потребоваться выполнять планирование для каждого склада по отдельности. Например, уровень страхового запаса товара и его политика дозаказа могут отличаться в зависимости от склада. В этом случае параметры планирования должны быть указаны для каждого товара и склада.  

Это поддерживается использованием единиц хранения, где можно задать отдельные параметры планирования на уровне единицы хранения. Единица хранения может рассматриваться как товар на определенном складе. Если пользователь не определил единицу хранения для этого склада, в программе будут использоваться параметры по умолчанию, заданные в карточке товара. Программа вычисляет план только для активных складов, где имеется существующий спрос или предложение данного товара.  

В принципе можно обработать любой товар не любом складе, но подход программы к понятию склада довольно строг. Например, заказ на продажу на одном складе невозможно выполнить с помощью определенного количества в наличии на другом складе. Количество в наличии необходимо сначала перевести на склад, указанный в заказе на продажу.  

![](media/NAV_APP_supply_planning_1_SKU_planning.png "NAV_APP_supply_planning_1_SKU_planning")  

Дополнительные сведения см. в разделе [Сведения о проектировании: перемещения при планировании](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Приоритет заказа  
В пределах заданной единицы хранения запрошенная или доступная дата представляет наивысший приоритет; спрос сегодняшнего дня необходимо удовлетворить перед спросом грядущих дней. Однако помимо данного типа приоритета, различные типы спроса и поставки сортируются согласно важности для организации для определения того, какой спрос следует удовлетворить сначала, прежде чем удовлетворять другой спрос. На стороне поставки приоритет заказа определяет, какой источник поставки следует применить до применения других источников поставки.  

Дополнительные сведения см. в разделе [Сведения о проектировании: определение приоритета заказов](design-details-prioritizing-orders.md).  

## <a name="production-forecasts-and-blanket-orders"></a>Прогнозы производства и общие заказы  
Прогнозы и общие заказы представляют предполагаемый спрос. Общий заказ, охватывающий предполагаемые покупки клиента за конкретный период времени, призван снизить неопределенность общего прогноза. Общий заказ — это прогноз по клиенту в дополнение к неопределенному прогнозу, как показано ниже.  

![](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "NAV_APP_supply_planning_1_forecast_and_blanket")  

Дополнительные сведения см. в подразделе "Прогнозируемый спрос снижается заказами на продажу" раздела [Сведения о проектировании: отправка профилей запасов](design-details-loading-the-inventory-profiles.md).  

## <a name="planning-assignment"></a>Назначение произ. плана  
Все товары должны быть запланированы, однако нет необходимости вычислять план для товара, если не было изменений в цепочке спрос-поставка с момента последнего расчета плана.  

Если пользователь ввел новый или изменил существующий заказ на продажу, есть причина выполнить перерасчет плана. Другие причины включают изменение в прогнозе или требуемом количестве страхового запаса. Изменение спецификации путем добавления или удаления компонента, скорее всего, укажет на изменение, но только для товара компонента.  

Система планирования осуществляет мониторинг таких событий и назначает соответствующие товары для планирования.  

При использовании нескольких складов назначение выполняется на уровне товара для каждой комбинации складов. Например, если заказ на продажу создан только на одном складе, программа назначит для планирования товар на данном конкретном складе.  

Причина выбора товаров для планирования — в производительности системы. Если цепочка спроса-поставки товара не была изменена, система планирования не предложит никаких действий. Без назначения планирования системе потребуется выполнять вычисления для всех элементов, чтобы определить, что можно планировать, а что истощит системные ресурсы.  

Полный список причин назначения товара системе планирования приводится в разделе [Сведения о проектировании: таблица "Назначение произ. плана"](design-details-planning-assignment-table.md).  

Параметры планирования в [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

-   Вычислить регенеративный план — вычисляются все выбранные товары независимо от того, требуется ли это.  
-   Вычислить план оборота — вычисляются только выбранные товары, цепочка спроса-поставки которых была изменена и которые, следовательно, были присвоены планированию.  

Некоторые пользователи считают, что планирование нетто-изменений должно выполняться мгновенно, например при вводе заказов на продажу. Однако это может привести к путанице, поскольку динамическая трассировка заказов и отправка сообщений о действиях также рассчитываются оперативно. Кроме того, [!INCLUDE[d365fin](includes/d365fin_md.md)] предлагает управление товарами, доступными для распределения, в реальном времени, то есть при вводе заказов на продажу, когда невозможно удовлетворить спрос по текущему плану поставок, отображаются всплывающие предупреждения.  

В дополнение к этому система планирования планирует только те товары, которые пользователь подготовил с использованием соответствующих параметров планирования. В противном случае предполагается, что пользователь запланирует товары вручную или в полуавтоматическом режиме с помощью функции планирования заказов.  

Дополнительные сведения о процедурах автоматического планирования см. в разделе [Сведения о проектировании: балансировка поставки и требований](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Измерения товара  
Спрос и поставка могут включать коды вариантов и коды складов, которые следует учитывать при балансировке спроса и поставки в системе планирования.  

Система рассматривает коды вариантов и складов как измерения товаров в строке заказа на продажу, операции журнала товаров и т. д. Соответственно, она рассчитывает план для каждой комбинации варианта и склада, как если бы комбинация была отдельным номенклатурным номером.  

Вместо расчета теоретической комбинации варианта и склада программа рассчитывает только комбинации, которые фактически существуют в базе данных.  

Дополнительные сведения о том, как система планирования обрабатывает коды складов в спросе, см. в разделе [Сведения о проектировании: спрос на пустом складе](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Атрибуты товаров  
Помимо общих измерений товаров, таких как номенклатурный номер, код варианта, код склада и тип заказа, каждое событие спроса и поставки может включать дополнительные спецификации в форме серийных номеров или номеров партий. Система планирования планирует эти атрибуты несколькими способами в зависимости от уровня спецификации.  

Связь "заказ-в-заказ" между спросом и поставкой — это еще один тип атрибута, который влияет на систему планирования.  

### <a name="specific-attributes"></a>Определенные атрибуты  
Некоторые атрибуты спроса являются специфическими и должны точно соответствовать определенной поставке. Существуют следующие два конкретных атрибута.  

-   Затребованные серийные номера/номера партий, требующие конкретного применения (установлен флажок **Трассировка СН** или **Партия - трассировка** в окне **Карточка кода трассировки товаров** для кода трассировки, используемого для товара).  
-   Связи с заказами на поставку, созданные вручную или автоматически для определенного спроса (ссылки "заказ-в-заказ").  

Для этих атрибутов система планирования применяет следующие правила:  

-   Спрос с определенными атрибутами может быть удовлетворен только поставкой с соответствующими атрибутами.  
-   Поставка с конкретными атрибутами также может удовлетворить спрос, для которого не требуются именно эти атрибуты.  

Соответственно, если запасов или прогнозируемых поставок недостаточно для того, чтобы удовлетворить спрос на определенные атрибуты, система планирования предложит новый заказ на поставку для удовлетворения данного спроса без учета параметров планирования.  

### <a name="non-specific-attributes"></a>Общие атрибуты  
Товары с серийными номерами или номерами партий без определенной настройки трассировки товаров могут включать серийные номера или номера партий, которые не требуется применять к определенному серийному номеру или номеру партии, но которые можно применить к любому серийному номеру или номеру партии. Это обеспечивает большую свободу системы планирования в сопоставлении, к примеру, серийного спроса и серийного предложения, как это обычно бывает в работе со складскими запасами.  

Определенные или неопределенные спрос и поставка с серийными номерами или номерами партий считаются высокоприоритетными и, следовательно, не включаются в замороженную зону, то есть они будут включены в планирование, даже если подлежат выполнению до даты начала планирования.  

Дополнительные сведения см. в подразделе "Серийные номера или номера партий загружаются по уровням спецификации" раздела [Сведения о проектировании: отправка профилей запасов](design-details-loading-the-inventory-profiles.md).  

Дополнительные сведения о том, как система планирования балансирует атрибуты, см. в подразделе «Серийные номера или номера партий и связи "заказ-в-заказ", исключенные из замороженной зоны» раздела [Сведения о проектировании: обработка заказов до даты начала планирования](design-details-dealing-with-orders-before-the-planning-starting-date.md).  

## <a name="order-to-order-links"></a>Связи "заказ-в-заказ"  
Приобретение "заказ-в-заказ" означает, что товар приобретается, собирается или производится исключительно для удовлетворения определенного спроса. Как правило, относится к товарам категории А. Мотивация для выбора такой политики — нерегулярный спрос, незначительное время подготовки или варьирование необходимых атрибутов.  

Еще одним особым случаем использования связи "заказ-в-заказ" является связь заказа на сборку с заказом на продажу в сценарии сборки на заказ.  

Связи "заказ-в-заказ" применяются между спросом и поставкой четырьмя способами:  

-   Если планируемый товар использует заказ политики повторного заказа.  
-   При использовании политики производства на заказ для создания многоуровневых производственных заказов или заказов проектного типа (производство необходимых компонентов в одном производственном заказе).  
-   При создании производственных заказов для заказов на продажу с использованием функции планирования заказа на продажу.  
-   При сборке товара по заказу на продажу. (Для политики сборки задано значение "Сборка на заказ".)  

В этих экземплярах система планирования предложит заказать только требуемое количество. После создания заказ на покупку, производственный заказ или заказ на сборку по-прежнему будет соответствовать определенному спросу. Например, если в заказе на продажу изменяется время или количество, система планирования предложит изменить связанный заказ на поставку соответствующим образом.  

При наличии связей между заказами система планирования не включает связанные поставки или запасы в процедуру уравновешивания. Пользователь оценивает, следует ли использовать связанную поставку для удовлетворения другого или нового спроса, и в данном случае следует ли удалить заказ на поставку или зарезервировать связанную поставку вручную.  

Резервирования и связи трассировки заказа будут нарушены при возникновении невозможной ситуации, например перемещения спроса на дату, предшествующую поставке. Однако связь заказ-в-заказ адаптируется к любым изменениям в соответствующем спросе или поставке, то есть связь никогда не нарушается.  

## <a name="reservations"></a>Резервирования  
Система планирования не включает зарезервированные количества в расчет. Например, если заказ на продажу был полностью или частично зарезервирован в соответствии с количеством в запасах, зарезервированное количество в запасах невозможно использовать для удовлетворения другого спроса. Система планирования не учитывает этот набор спроса и предложения в расчете.  

Однако система планирования все же будет включать зарезервированные количества в профиле прогнозируемых запасов, поскольку все количества должны учитываться при определении времени перехода точки дозаказа и количества дозаказа для достижения, но не превышения максимального уровня запасов. Следовательно, ненужные резервирования приведут к увеличению риска снижения уровня запасов, поскольку логика планирования не обнаруживает зарезервированные количества.  

На следующей иллюстрации показано, как резервирования могут помешать реализации даже самого реалистичного плана.  

![](media/NAV_APP_supply_planning_1_reservations.png "NAV_APP_supply_planning_1_reservations")  

Дополнительные сведения см. в разделе [Сведения о проектировании: резервирование, трассировка заказов и отправка сообщений о действиях](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Предупреждения  
Первый столбец в таблице планирования — для полей предупреждений. Во всех строках планирования, созданных для нестандартной ситуации, в этом поле будет отображаться значок предупреждения, щелкнув который можно получить дополнительную информацию.  

Поставка в строках планирования с предупреждениями обычно не изменяется в соответствии с параметрами планирования. Вместо этого, система планирования только предлагает поставку для покрытия конкретного требуемого количества. Однако систему можно настроить таким образом, чтобы использовались определенные параметры планирования для строк планирования с определенными предупреждениями. Дополнительные сведения см. в описании этих параметров для пакетного задания **Расчет плана - журнал планов** и пакетного задания **Расчет плана - журнал потребности** соответственно.  

Предупреждающее сообщение отображается в окне **Неотслеживаемые элементы планирования**, которое также используется дл отображения строк трассировки заказа сущностям вне сети заказов. Существуют следующие типы предупреждений:  

-   Экстренный,  
-   Исключение  
-   Внимание!  

![](media/NAV_APP_supply_planning_1_warnings.png "NAV_APP_supply_planning_1_warnings")  

### <a name="emergency"></a>Экстренный,  
Экстренное предупреждение отображается в двух случаях:  

-   Если запасы отрицательные на планируемую дату начала.  
-   Если существуют события спроса или поставки, датированные прошедшим числом.  

В случае отрицательных запасов товара на планируемую дату начала система планирования предложит экстренную поставку с количеством, равным отрицательному остатку, и поставкой на планируемую дату начала. В тексте предупреждения указывается дата начала и количество для экстренного заказа. Дополнительные сведения см. в разделе [Сведения о проектировании: обработка прогнозируемых отрицательных остатков](design-details-handling-projected-negative-inventory.md).  

Любые строки документа с датами завершения до планируемой даты начала объединяются в один экстренный заказ на поставку товара с доставкой на планируемую дату начала.  

### <a name="exception"></a>Исключение,  
Предупреждение об исключении отображается в случае, когда прогнозируемые доступные запасы оказываются ниже количества страхового запаса. Система планирования предложит заказ на поставку для выполнения требования к сроку выполнения. В тексте предупреждения указывается количество страхового запаса товара и дата на которую произошло данное нарушение.  

Нарушение требования к уровню страхового запаса считается причиной исключения, так как в случае правильной настройки точки повтора заказа такая ситуация возникать не должна. Дополнительные сведения см. в разделе [Сведения о проектировании: роль точки дозаказа](design-details-the-role-of-the-reorder-point.md).  

В целом, исключительные предложения заказа обеспечивают достаточное количество ожидаемого доступного запаса, который не опустится ниже уровня страхового запаса. Это означает, что предложенного количества едва достаточно для покрытия страхового запаса без учета параметров планирования. Однако в некоторых сценариях будут учитываться модификаторы заказа.  

> [!NOTE]  
>  Возможно, система планирования израсходовала страховой запас намеренно, и он будет немедленно пополнен. Дополнительные сведения см. в подразделе "Страховой запас может быть использован" раздела [Сведения о проектировании: отправка профилей запасов](design-details-loading-the-inventory-profiles.md).

### <a name="attention"></a>Внимание!  
Предупреждение о необходимости обратить на что-либо внимание отображается в трех случаях:  

-   планируемая дата начала наступает раньше рабочей даты;  
-   В строке планирования предлагается изменить выпущенный заказ на покупку или производственный заказ.  
-   Прогнозируемый запас превышает допустимый избыток на дату оплаты. Дополнительные сведения см. в разделе [Сведения о проектировании: нахождение ниже уровня допустимого избытка](design-details-staying-under-the-overflow-level.md).  

> [!NOTE]  
>  В строках планирования с предупреждениями поле **Принять указания** не выбрано, так как ожидается, что планировщик дополнительно изучит эти строки перед составлением плана.  

## <a name="error-logs"></a>Журналы ошибок  
На странице запроса "Вычислить план" пользователь может выбрать поле **Остановить и показать первую ошибку**, чтобы остановить процесс планирования при возникновении первой ошибки. Одновременно отобразится сообщение со сведениями об этой ошибке. Если существует ошибка, в журнале планирования будут показаны только правильные строки планирования, завершенные до выявления ошибки.  

Если поле не выбрано, пакетное задание "Вычислить план" будет выполняться до завершения. Ошибки не приведут к прерыванию пакетного задания. При возникновении одной или нескольких ошибок программа выводит сообщение о том, сколько товаров было затронуто ошибками. Затем откроется окно **Журнал ошибок планирования**, содержащее дополнительные сведения об ошибке и ссылки на соответствующие документы и карточки товаров.  

![](media/NAV_APP_supply_planning_1_error_log.png "NAV_APP_supply_planning_1_error_log")  

## <a name="planning-flexibility"></a>Гибкость планирования  
Не всегда практично планирование существующего заказа на поставку, например если начато производство или нанят дополнительный персонал в определенный день для выполнения задания. Чтобы обозначить, можно ли изменить существующий заказ системой планирования, все строки заказа на поставку имеют поле "Гибкость планирования" с двумя параметрами: "Неограниченная" и "Нет". Если в данном поле задано значение "Нет", система планирования не будет пытаться изменить строку заказа на поставку.  

Пользователь может вручную настроить это поле, однако в некоторых случаях оно будет вручную настраиваться системой. Очень важен тот факт, что гибкость планирования можно вручную настроить пользователем, потому что это упрощает адаптацию применения этой функции к разным рабочим процессам и бизнес-случаям.  

Дополнительные сведения об использовании этого поля см. в разделе [Сведения о проектировании: перемещения при планировании](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Планирование заказов  
Основной инструмент планирования, представленный в окне **Планирование заказов**, предназначен для неавтоматизированного принятия решений. В нем не учитываются параметры планирования, и, следовательно, оно не рассматривается далее в этом документе. Дополнительные сведения о функции планирования заказов см. в справке по [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Не рекомендуется использование раздела "Планирование заказов ", если организация уже использует формы заявок или планирования. Заказы на поставку, созданные в окне **Планирование заказов**, могут быть изменены или удалены в процессе автоматического планирования. Это может произойти из-за того, что в процессе автоматического планирования используются параметры планирования, которые могут не учитываться пользователем, выполняющим планирование вручную в окне "Планирование заказов".  

##  <a name="finite-loading"></a>Ограниченная загрузка  
[!INCLUDE[d365fin](includes/d365fin_md.md)] является стандартной системой ERP, а не системой управления отправкой или системой управления цехом. Она планирует возможное использование ресурсов, предоставляя приблизительный график, но не создает и не поддерживает подробные графики автоматически на основе приоритетов или правил оптимизации.  

Функция ограничения ресурса производственной мощности предусмотрена для использования следующим образом: 1) чтобы избежать перегрузки ресурса и 2) обеспечить распределение всех производственных ресурсов, если это позволило бы ускорить время выполнения производственного заказа. Эта функция не предоставляет механизмов или возможностей определения приоритетности или оптимизации операций, как этого можно было бы ожидать от диспетчерской системы. Однако она может предоставить черновые сведения о производственных мощностях, полезные для определения узких мест и избежания перегрузки ресурсов.  

При планировании с ограниченными по мощности ресурсами система гарантирует, что ни один ресурс не загружается с превышением определенной производственной мощности (критическая загрузка). Это выполняется путем назначения каждой операции ближайшему доступному временному интервалу. Если временной интервал недостаточно продолжительный для завершения всей операции, операция будет разделена на две или более частей, помещенных в ближайшие доступные временные интервалы.  

> [!NOTE]  
>  В случае разделения операций время настройки назначается только один раз, поскольку предполагается, что выполняются некоторые коррекции вручную для оптимизации графика.  

Буферный период можно добавить к ресурсам для сведения к минимуму разделения операций. Это позволяет системе планировать загрузку на последний возможный день с небольшим превышением процента критической нагрузки, если при этом число разделяемых операций будет уменьшено.  

Это завершает обзор основных концепций, связанных с планированием поставок в [!INCLUDE[d365fin](includes/d365fin_md.md)]. В следующих разделах эти понятия рассматриваются более подробно и в контексте базовых процедур планирования и балансировки спроса и предложения, а также использования политик повторных заказов.  

## <a name="see-also"></a>См. также  
[Сведения о проектировании: перемещения при планировании](design-details-transfers-in-planning.md)   
[Сведения о проектировании: параметры планирования](design-details-planning-parameters.md)   
[Сведения о проектировании: таблица "Назначение произ. плана"](design-details-planning-assignment-table.md)   
[Сведения о проектировании: обработка политик дозаказа](design-details-handling-reordering-policies.md)   
[Сведения о проектировании: балансировка спроса и поставки](design-details-balancing-demand-and-supply.md)
