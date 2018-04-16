---
title: "Использование расширения \"Миграция данных C5\" | Microsoft Docs"
description: "Используйте это расширение для переноса клиентов, поставщиков, товаров и счетов главной книги из Microsoft Dynamics C5 2012 в Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7fe6393ad43dbad032512b2d6d45cc8ee0392236
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a>Расширение "Миграция данных C5" для Business Central
Это расширение упрощает перенос клиентов, поставщиков, товаров и ваших счетов главной книги из Microsoft Dynamics C5 2012 в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Также можно перенести архивные операции для счетов главной книги.

> [!Note]
> Организация в [!INCLUDE[d365fin](includes/d365fin_md.md)] не должна содержать никаких данных. Кроме того, после запуска миграции не создавайте клиентов, поставщиков, товаров или счетов, пока миграция не закончит работу.

##<a name="what-data-is-migrated"></a>Какие данные можно перенести?
Следующие данные можно перенести для каждого объекта:

**Клиенты**
* Склады
* Страна
* Измерения клиента (отдел, центр, назначение)
* Метод поставки
* Продавец
* Условия оплаты
* Способ оплаты
* Ценовая группа клиента
* Скидка по счету клиента

При переносе учетной записи также переносятся следующие данные:

* Настройка учета клиента
* Раздел финансового журнала
* Открытые транзакции (операции книги клиентов)

**Поставщики**
* Склады
* Страна
* Измерения поставщика (отдел, центр, назначение)
* Скидка по счету
* Метод поставки
* Закупщик
* Условия оплаты
* Способ оплаты
* Скидка по счету поставщика

При переносе учетной записи также переносятся следующие данные:

* Настройка учета поставщика
* Раздел финансового журнала
* Открытые транзакции (операции книги поставщиков)

**Товаров**
* Склады
* Страна
* Измерения товара (отдел, центр, назначение)
* Скидки строки продаж
* Группы скидок клиента
* Группы скидок по товару
* Цена продажи
* Код тарифа
* Единицы измерения
* Код трассировки товара
* Ценовая группа клиента

При переносе учетной записи также переносятся следующие данные:

* Настройка учета запасов
* Общая настройка учета
* Раздел журнала товаров
* Открытые транзакции (операции книги товаров)

> [!Note]
> При наличии открытых транзакций, использующих иностранные валюты, также переносятся валютные курсы для этих валют. Другие валютные курсы не переносятся.

## <a name="to-migrate-data"></a>Для миграции данных
Для экспорта данных из C5 и импорта их в [!INCLUDE[d365fin](includes/d365fin_md.md)] нужно выполнить всего несколько шагов:  

1. В C5, используйте функцию **Экспорт базы данных**, чтобы экспортировать данные. Затем отправьте папку экспорта в сжатую (ZIP) папку.  
2. В [!INCLUDE[d365fin](includes/d365fin_md.md)] выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Миграция данных**, затем выберите **Миграция данных**.  
3. Выполните шаги облегчить в мастере настройки. Обязательно выберите в качестве источника данных **Импорт из Microsoft Dynamcis C5 2012**.  

> [!Note]
> Организации часто добавляют поля для настройки C5 для определенной сферы деятельности. [!INCLUDE[d365fin](includes/d365fin_md.md)] не производит миграцию данных из настраиваемых полей. Кроме того, миграция потерпит неудачу, если имеется более 10 настраиваемых полей.

## <a name="viewing-the-status-of-the-migration"></a>Просмотр состояния миграции
Используйте страницу **Обзор миграции данных** для контроля успешности миграции. На этой странице отображается такая информация, как количество объектов, которые будут включены в миграцию, состояние миграции, количество элементов, для который была произведена миграция, и была ли эта миграция успешной. Также отображается число ошибок, позволяет вам определить, что пошло неправильно, и, когда это возможно, позволяет легко перейти к объекту для устранения проблем. Дополнительные сведения см. в следующем разделе этой статьи.  

> [!Note]
> Пока результаты миграции еще ожидаются, следует обновить страницу для отображения результатов.

## <a name="correcting-errors"></a>Исправление ошибок
Если что-то пошло не так и возникли ошибки, в поле **Состояние** отображается **Завершено с ошибками**, а в поле **Число ошибок** отображается количество ошибок. Для просмотра списка ошибок можно открыть страницу **Ошибки миграции данных**, выбрав:  

* Номер в поле **Число ошибок** для объекта.  
* Объект, затем действие **Показать ошибки**.  

На странице **Ошибки миграции данных** чтобы исправить ошибку, можно выбрать сообщение об ошибке, затем выбрать **Изменить запись** для открытия страницы, которая показывает перенесенные данные для объекта. После исправления одной или нескольких ошибок можно выбрать **Миграция**, чтобы выполнить перенос только исправленных объектов, без необходимости полного повторного выполнения миграции.  

> [!Tip]
> Если исправлено несколько ошибок, можно использовать функцию **Выбрать больше**, чтобы выбрать несколько строк для миграции. Если же ошибки не важны и их можно не исправлять, можно выбрать их, затем выбрать **Пропустить выбранные элементы**.

> [!Note]
> Если имеются товары, которые включены в спецификацию, может возникнуть необходимость выполнить миграцию несколько раз, если исходный товар не был создан до вариантов, которые ссылаются на него. Если сначала создается вариант товара, то ссылка на исходный товару может привести к появлению сообщения об ошибке.  

## <a name="verifying-data-after-migrating"></a>Проверка данных после миграции
Если требуется проверять правильность миграции данных, можно просмотреть следующие страницы в C5 и [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|Объекты клиента| Финансовые журналы|
|Объекты поставщика| Финансовые журналы|
|Операции товара| Журналы товаров|

В [!INCLUDE[d365fin](includes/d365fin_md.md)] пакет для перенесенных данных называется **C5MIGRATE**.

## <a name="stopping-data-migration"></a>Остановка миграции данных
Можно остановить миграцию данных, выбрав **Остановить все операции миграции**. Если это сделать, все ожидающие операции миграции также будут остановлены.

## <a name="see-also"></a>См. также
[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью расширений](ui-extensions.md)  
[Приступая к работе](product-get-started.md) 
