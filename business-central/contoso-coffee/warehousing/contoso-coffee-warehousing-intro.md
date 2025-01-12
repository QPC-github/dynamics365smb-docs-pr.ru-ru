---
title: Знакомство с Contoso Coffee
description: 'Обзор сценариев, в которых демонстрационные данные Contoso Coffee могут помочь вам узнать, как использовать возможности Business Central для склада.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-warehousing" />Знакомство со складским хозяйством Contoso Coffee

Contoso Coffee — вымышленная компания, производящая бытовые и коммерческие кофеварки. Приложения **Contoso Coffee** для Business Central добавляют демонстрационные данные, которые вы можете использовать, чтобы узнать, как использовать возможности Business Central для складского дела. Вы можете настраивать складские функции различными способами, см. [Обзор различных вариантов настройки](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Приложение предоставляет три склада, которые оптимизированы для разных сценариев:

- **СЕРЕБР.**  

  Для этого склада настроено использование ячеек. Его можно легко настроить для поддержки базовой или расширенной конфигурации. 

- **ЖЕЛТЫЙ**  

  Для этого склада используется расширенная конфигурация склада, но не используются ячейки. Его можно перенастроить для поддержки базовых конфигураций.

- **БЕЛЫЙ**  

  Для этого склада используется расширенная конфигурация склада с расширенными подбором и размещением, что позволяет использовать более сложные правила перемещения товаров по складу.

## <a name="set-up-contoso-coffee-warehousing-data" />Настройка данных Contoso Coffee для склада

Чтобы можно было использовать демонстрационные складские данные Contoso Coffee, необходимо установить два приложения в соответствующей компании в [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Набор демонстрационных данных Contoso Coffee**  

    Это приложение предоставляет демонстрационные данные для базового приложения.  
- **Демонстрационный набор данных Contoso Coffee (идентификатор страны/региона)**  

    \Это приложение добавляет контент для конкретной страны/региона поверх базового приложения.

Добавьте приложения в пустую компанию в платной подписке или в рамках пробной версии. Например, создайте новую компанию без демонстрационных данных в мастере настройки **Создать новую компанию**, который можно открыть в списке **Компании**. Затем добавьте приложения из [рынка](../../ui-extensions-install-uninstall.md#install), если они еще не указаны на странице **Управление расширениями**.  

После установки соответствующих приложений перейдите на страницу [Демонстрационные складские данные Contoso Coffee](https://businesscentral.dynamics.com/?page=4761) в [!INCLUDE [prod_short](../../includes/prod_short.md)] и измените настройки по умолчанию в соответствии с вашими потребностями. Параметры рассматриваются в таблице ниже:  

|Поле  |Описание  |
|---------|---------|
|**Начальный год** |Указывает первый год, который вы хотите использовать для демонстрационных данных Contoso Coffee. В зависимости от настройки компании год может быть либо календарным, либо финансовым годом.|
|**Склад — ячейка**  |Склад для использования в сценариях базового склада.|
|**Склад — расш. логистика**  |Склад для использования в сценариях с простой логистикой.|
|**Склад — расширенные подбор и размещение**  |Склад для использования в сценариях с расширенной логистикой.|
|**Склад — транзит**  |Склад для использования в сценариях, в которых для перемещения используется транзитный склад.|
|**Клиент Но.**  |Клиент, используемый в базовых и простых сценариях операций продаж.|
|**№ поставщика**  |Поставщик, используемый для всех сценариев операций закупок.|
|**Основной инв. номер**  |Товар, используемый для всех сценариев операций продаж.|
|**Инв. номер товара 1**  |Основной товар, используемый для всех сценариев.|
|**Инв. номер товара 2**  |Дополнительный товар, используемый для всех сценариев.|
|**Учетная группа клиента**|Указывает бизнес-код для внутренних клиентов. Бизнес-коды используются при учете транзакций. |
|**Общая учетная бизнес-группа для клиента**|Указывает бизнес-код для внутренних клиентов. Бизнес-коды используются при учете транзакций. |
|**Учетная группа поставщика**|Указывает бизнес-код для внутренних клиентов и поставщиков. Бизнес-коды используются при учете транзакций. |
|**Общая учетная бизнес-группа для поставщика**|Указывает бизнес-код для внутренних клиентов и поставщиков. Бизнес-коды используются при учете транзакций. |
|**Внутр. — учетная бизнес-группа НДС**|Указывает бизнес-код НДС для клиентов и поставщиков для учета НДС, если НДС включен.|
|**Перепродажа — учетная группа товаров**    |Указывает код для товаров, которые должны использоваться для учета перепродажи.|
|**Розница - Общая товарная группа**    |Указывает код для товаров, которые должны использоваться для учета розницы.|
|**НДС Товарная Группа**    |Указывает код продукта НДС для товаров для учета НДС, если НДС включен.|
|**Ценовой фактор**     |Указывает коэффициент для конвертации цены из долларов США/евро в местную валюту. *1* означает, что цена — это одинаковая сумма в любой валюте. Для получения цены в местной валюте будет использоваться более высокое число. |
|**Точность округления**  |Определяет порядок округления рассчитанных потребляемых количеств при вводе в строки журнала потребления. Количества меньше 0,5 будут округляться в меньшую сторону. Количества, равные или больше 0,5, будут округляться в большую сторону.|

Когда будете готовы, выберите действие **Создать демонстрационные данные**. Добавление данных в базовую базу данных занимает несколько минут, но затем вы можете запускать различные сценарии.  

> [!IMPORTANT]
> Если вы используете сценарии, рекомендуем убедиться, что ваш пользователь добавлен для выбранных складов. Дополнительные сведения см. в разделе [Настройка работников склада](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios" />Сценарии

В настоящее время демонстрационные складские данные Contoso Coffee поддерживают следующие сценарии тестирования и обучения:

1.  [Пошаговое руководство. Приход и расход в базовых конфигурациях склада](warehouse-basic-flow-putaway-pick.md)
2.  [Пошаговое руководство. Приход и расход в смешанных конфигурациях склада](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Пошаговое руководство. Приход и расход в расширенных конфигурациях склада с расширенным подбором и размещением](warehouse-directed-flow.md)

Прочитайте шаги для каждого сценария в соответствующей статье.  

## <a name="see-also" />См. также

[Настройка запасов](../../inventory-setup-inventory.md) 
[Как настраивать склады](../../inventory-how-setup-locations.md) 
[Складское хозяйство](../../warehouse-manage-warehouse.md) 
[Сведения о проектировании](../../design-details-warehouse-overview.md) 
