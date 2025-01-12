---
title: Расширение миграции данных QuickBooks Online
description: 'Описывает, как использовать расширение для миграции клиентов, поставщиков, товаров и счетов из QuickBooks Online в Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'extension, migrate, data, QuickBooks, import'
ms.search.form: '1830,'
ms.date: 06/24/2021
ms.author: bholtorf
---

# <a name="the-quickbooks-online-data-migration-extension" />Расширение миграции данных QuickBooks Online

Это расширение входит в руководстве по сопровождаемой настройке **Миграция данных**, которое помогает переносить важные бизнес-данные из QuickBooks Online в [!INCLUDE[prod_short](includes/prod_short.md)]. Например, это бывает полезно, если ваш бизнес расет, и вы решили обновить свое приложение для управления бизнесом и перейти на [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-data-can-i-import-from-quickbooks-online" />Какие данные можно импортировать из QuickBooks Online?

Можно импортировать следующие данные из QuickBooks Online в [!INCLUDE[prod_short](includes/prod_short.md)]:  

* Клиенты
* Поставщики
* Товаров
* План счетов
* Транзакция начального сальдо в главной книге
* Товары в наличии
* Открытые документы для клиентов и поставщиков, например счета, кредит-ноты и платежи

Мы переносим только полные суммы документов продажи и покупки. Мы не обновляем частично оплаченные суммы. Например, если клиент оплатил 300 долларов из 500 по счету продажи, мы переносим 500 долларов. Если вы получили частичные платежи, их необходимо вручную обновить либо до миграции данных, либо после нее. Рекомендуется применить незакрытые транзакции перед миграцией, чтобы потом было проще работать.

> [!NOTE]  
> Мы не переносим заказы на покупку и заказы на продажу.

## <a name="before-you-start" />Перед началом работы

Важной частью процесса миграции является указание счетов, на которые должны быть перенесены транзакции. Рекомендуется задать сопоставление до переноса данных. Например, задать счета, на которых вы учитываете транзакции для:  

* Продажи товаров или услуг клиентам.
* Покупки товаров или услуг у поставщиков.  
* Коррекции в главной книге.  

[!INCLUDE[prod_short](includes/prod_short.md)] требует, чтобы счетам главной книги были назначены номера. Убедитесь, что номера счетов назначены в QuickBooks Online.

Если транзакции в QuickBooks Online содержат суммы налога, необходимо настроить налоговый счет в налоговых юрисдикциях в [!INCLUDE[prod_short](includes/prod_short.md)], прежде чем вы сможете учитывать транзакции.

## <a name="how-do-i-start-using-the-extension" />Как начать использование расширения?

Начать очень просто. Вам достаточно запустить руководство по сопровождаемой настройке **Миграция данных**. Вот как это сделать:

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Мастер настройки**, а затем выберите **Миграция бизнес-данных**.
2. На каждом этапе следуйте инструкциям руководства по сопровождаемой настройке.

## <a name="what-do-i-do-after-i-migrate-data" />Что нужно сделать после переноса данных?

После переноса данных транзакции имеют статус **Неучтенные**, чтобы их можно было проверить и внести корректировки. Чтобы проверить транзакции, откройте страницу, на которой они должны находиться. Например, чтобы проверить неучтенные счета продажи, перейдите на страницу **Счета продажи**. Чтобы проверить журналы платежей, перейдите на страницу **Журналы платежей**.  

Есть несколько важных вещей, которые нужно сделать.

* Если для транзакций в QuickBooks Online были заданы суммы наценки или скидки, их необходимо вручную добавить в соответствующие транзакции в [!INCLUDE[prod_short](includes/prod_short.md)], прежде чем учитывать их.
* Если вы используете налог на добавленную стоимость (НДС), вы можете добавить учетные бизнес-группы или товарные группы в параметры учета, чтобы вы могли учитывать суммы НДС.
* Проверьте начальные сальдо счетов в главной книге. В QuickBooks Online не хранится текущее сальдо для всех счетов, поэтому вам может потребоваться исправить начальные сальдо.

## <a name="see-related-microsoft-trainingtrainingmodulesmigrate-data-dynamics-365-business-central" />См. соответствующее [обучение Microsoft](/training/modules/migrate-data-dynamics-365-business-central/)

## <a name="see-also" />См. также

[Импорт бизнес-данных из других финансовых систем](across-import-data-configuration-packages.md)  
[Настройка [!INCLUDE[prod_short](includes/prod_short.md)] с помощью расширений](ui-extensions.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
