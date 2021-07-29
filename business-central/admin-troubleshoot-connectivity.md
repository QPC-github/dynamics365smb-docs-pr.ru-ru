---
title: Устранение неполадок с подключением
description: Описывает, как использовать страницу "Устранение неполадок подключения" для выявления и устранения проблем с подключением к Business Central Online.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: connectivity, troubleshooting, connection problems
ms.date: 06/17/2021
ms.author: jswymer
ROBOTS: NOINDEX
ms.openlocfilehash: db7b9e602817d7dddcf6bce1b35ede078bd70aa0
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443185"
---
# <a name="troubleshoot-connectivity-for-business-central"></a>Устранение неполадок подключения для Business Central

> **ОТНОСИТСЯ К:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Эта функция в настоящее время доступна для предварительного ознакомления. Функциональные возможности и документация могут измениться в более поздних версиях. Если вы хотите внести свой вклад в документацию на основе собственных выводов, выберите ![Изменить статью на GitHub.](media/github-edit-pencil.png) **Редактировать**, и предложите изменения. Давайте посмотрим!

[!INCLUDE[prod_short](includes/prod_short.md)] онлайн содержит страницу **Устранение неполадок с подключением**, которую можно использовать для выявления проблем с подключением к онлайн-службе. Есть несколько вещей, которые влияют на подключение к Business Central, например, настройки брандмауэра вашей сети или конфигурация службы доменных имен. На этой странице можно запустить список проверок, которые позволят диагностировать типичные проблемы с подключением к Business Central. Вы можете использовать эту информацию, чтобы попытаться решить проблемы самостоятельно, или передать ее представителю службы поддержки.

> [!NOTE]
> Страница **Устранение неполадок с подключением** не проверяет производительность или надежность сети, например скорость вашего соединения. Только проверяется подключение к разным ресурсам.

## <a name="start-the-connectivity-check"></a>Начать проверку подключения 

1. Нажмите [эту ссылку](https://businesscentral.dynamics.com/connectivity) или откройте свой интернет-браузер и вставьте следующий URL-адрес в адрес:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

2. На странице **Устранение неполадок с подключением** выберите **Начать проверку**.

    Выполняется серия проверок, и отображается результат каждой проверки:

    - ![Проверка подключения прошла успешно.](media/connectivity-check.png) указывает, что проверка прошла успешно.
    - ![Проверка подключения не пройдена.](media/connectivity-failed.png) указывает, что проверка завершилась неудачно. Просмотрите сообщение ниже для получения дополнительных сведений.
    - ![Проверка подключения не выполнялась.](media/connectivity-blocked.png) указывает, что проверка не выполнялась, обычно из-за сбоя предыдущей проверки. Просмотрите сообщение ниже для получения дополнительных сведений.

3. Чтобы снова запустить проверку, выберите **Перезапустить проверку**.

В следующих разделах объясняются выполняемые проверки и даются советы по устранению проблем.

## <a name="basic-internet-connectivity"></a>Базовое подключение к Интернету

Проверяет, есть ли у вас подключение к Интернету, подтверждая, что у вас есть доступ к известному общедоступному домену, например www.bing.com.

|Проблема|Что стоит попробовать|
|-------|-------------|
|Ваш браузер не поддерживает эту проверку|Откройте страницу в поддерживаемом браузере и попробуйте еще раз. Список поддерживаемых браузеров смотрите в [Минимальные требования для использования Business Central — браузеры](product-requirements.md#browsers)|
|Не удалось проверить связь с сервером по следующему URL-адресу: {url}|Проверьте настройки брандмауэра.|

## <a name="cdn-content-delivery-network-resources-loading"></a>Загрузка ресурсов CDN (сети доставки контента)

[!INCLUDE[prod_short](includes/prod_short.md)] использует сеть доставки контента Azure (CDN) для предоставления ресурсов, необходимых для запуска веб-клиента Business Central. Эта проверка проверяет наличие и доступность необходимых ресурсов путем проверки связи с экземпляром Business Central в CDN.

|Проблема|Что стоит попробовать|
|-------|-------------|
|Ваш браузер не поддерживает эту проверку|Смотрите проверку **Базовое подключение к Интернету**.|
|Не удалось проверить связь с сервером по следующему URL-адресу: {url}|Проверьте настройки брандмауэра.|

## <a name="user-authentication"></a>Аутентификация пользователя

Проверяет, что текущий пользователь вошел в систему с действующей учетной записью Business Central.

|Проблема|Что стоит попробовать|
|-------|-------------|
|В настоящее время ни один пользователь не аутентифицирован|Войдите в Business Central с действующим именем пользователя и паролем.|

## <a name="business-central-environments-discovery"></a>Обнаружение сред Business Central

Проверяет наличие сред Business Central, доступных для аутентифицированного пользователя, а затем проверяет, может ли пользователь пройти аутентификацию в среде.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Проблема|Что стоит попробовать|
|-------|-------------|
|Нет аутентифицированного пользователя для выполнения этой проверки|Перейдите к проверке **Аутентификация пользователя**.|
|Не удалось получить доступные среды для вашей учетной записи.|Проверьте список доступных сред в центре администрирования Business Central.|
|Ваше имя пользователя или пароль неверны, или у вас нет действительной учетной записи.| Убедитесь, что вы вошли в систему, используя правильное имя пользователя и пароль.|

## <a name="application-service-connectivity"></a>Подключение к службе приложений

Проверяет, может ли аутентифицированный пользователь подключиться к обнаруженной среде, обычно начиная с производственной среды.

|Проблема|Что стоит попробовать|
|-------|-------------|
|Нет аутентифицированного пользователя для выполнения этой проверки|Перейдите к проверке **Аутентификация пользователя**.|
|Не удалось получить доступные среды для вашей учетной записи.|Прочитайте **Обнаружение сред Business Central**.|
|Нет адреса кластера для выполнения этой проверки|Проверьте список доступных сред в центре администрирования Business Central.|
|Конечная точка версии не существует|Проверьте список доступных сред в центре администрирования Business Central.|

## <a name="see-also"></a>См. также

[Ресурсы для справки и поддержки](product-help-and-support.md)  
[Обзор задач для настройки Business Central](setup.md)  
[Вопросы и ответы об использовании Business Central](across-faq.yml)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Центр администрирования Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]