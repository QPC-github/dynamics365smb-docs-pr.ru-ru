---
title: Создание и настройка учетной записи Shopify
description: 'Узнайте, как получить учетную запись Shopify, чтобы продемонстрировать рабочий процесс интеграции Shopify и Business Central.'
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# Создание и настройка учетной записи Shopify

Если вы рассматриваете возможность использования Shopify в качестве решения для электронной коммерции и вам нужна учетная запись Shopify для проверки интегрированного рабочего процесса, вы можете поступить следующим образом:

- Получить пробную версию. Это типичная отправная точка для конечных пользователей.  
- Создать магазины разработки. Этот подход предназначен для партнеров, которые регулярно проводят демонстрации, тренинги и оказывают поддержку.

## Пробная версия (конечный пользователь)

Перейдите на [веб-сайт Shopify](https://www.shopify.com) и используйте свою учетную запись электронной почты в качестве учетной записи администратора, чтобы подписаться на бесплатную пробную версию. Подробнее о том, как создать и персонализировать свой интернет-магазин, см. в [справочном центре Shopify](https://help.shopify.com/).

В разделе **Администрирование Shopify** созданного магазина примените следующие **Настройки**:

- Деактивируйте параметр **Автоматически архивировать заказ** в разделе **Обработка заказов** в настройках [**Оформление заказа**](https://www.shopify.com/admin/settings/checkout) в **центре администрирования Shopify**.
- Рассмотрите возможность включения параметра *Показывать ссылку для входа на витрине и при оформлении заказа* в разделе **Настройки учетной записи клиента** в настройках оформления заказа.
- Рекомендуем выбрать параметр *Название компании — необязательно* в разделе **Информация о клиенте** в настройках оформления заказа.
- Включите параметр **Показывать варианты чаевых при оформлении заказа** в разделе **Чаевые** в параметрах оформления заказа, если вы планируете демонстрировать чаевые.
- Активировать тестовые платежи. В этом случае у вас есть два варианта. Для начала перейдите в параметры [**Платежей**](https://www.shopify.com/admin/settings/payments):  
  1. *(для тестирования) Bogus Gateway*. Дополнительные сведения см. в разделе [Активация Bogus Gateway для тестирования](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* в режиме тестирования. Дополнительные сведения см. в разделе [Тестирование Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Выберите план в параметрах [**План**](https://www.shopify.com/admin/settings/plan), чтобы протестировать процесс оплаты.

> [!Important]  
> Чтобы избежать платежей, не забудьте отменить пробную версию Shopify.

## Магазин разработки

Начните с присоединения к [Партнерской программе Shopify](https://help.shopify.com/partners/about). После этого используйте **Панель мониторинга партнера**, чтобы создать магазин разработки. Подробнее см. в статье [Создание магазинов разработки](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

После создания магазина в разделе **Администрирование Shopify** созданного магазина примените следующие **Настройки**:

- Деактивируйте параметр **Автоматически архивировать заказ** в разделе **Обработка заказов** в настройках [**Оформление заказа**](https://www.shopify.com/admin/settings/checkout) в **центре администрирования Shopify**.
- Рассмотрите возможность включения параметра *Показывать ссылку для входа на витрине и при оформлении заказа* в разделе **Настройки учетной записи клиента** в настройках оформления заказа.
- Рекомендуем выбрать параметр *Название компании — необязательно* в разделе **Информация о клиенте** в настройках оформления заказа.
- Включите параметр **Показывать варианты чаевых при оформлении заказа** в разделе **Чаевые** в параметрах оформления заказа, если вы планируете демонстрировать чаевые.
- Активировать тестовые платежи. В этом случае у вас есть два варианта. Для начала перейдите в параметры [**Платежей**](https://www.shopify.com/admin/settings/payments):  
  1. *(для тестирования) Bogus Gateway*. Дополнительные сведения см. в разделе [Активация Bogus Gateway для тестирования](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* в режиме тестирования. Подробнее см. в разделе [Тестирование Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

## См. также

[Начало работы с соединителем Shopify](get-started.md)  
[Пошаговое руководство: настройка и использование соединителя Shopify](walkthrough-setting-up-and-using-shopify.md)