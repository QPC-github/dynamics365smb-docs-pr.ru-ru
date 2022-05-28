---
title: Получение Business Central на настольном компьютере
description: В этой статье описывается, как установить приложение Business Central на настольный компьютер Windows или MACiOS.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: phone, tablet
ms.date: 01/11/2022
ms.author: jswymer
ms.openlocfilehash: 3e04e348c55fa487f8a7776c0f197210c3cacb49
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519756"
---
# <a name="get-business-central-desktop-app"></a>Получение приложения Business Central на настольном компьютере

Если у вас есть компьютер с Windows (ПК) или macOS, вы можете установить приложение Business Central на свой настольный компьютер. Приложение работает с Business Central Online и локально.

## <a name="why-use-the-app"></a>Почему нужно использовать это приложение?

Приложение Business Central похоже на веб-клиент, но имеет несколько преимуществ, например:

- Приложение доступно в меню **Пуск**, вы можете легко закрепить его на панели задач или запустить по умолчанию при запуске компьютера.
- В целом, приложение также быстрее и плавнее отображается на экране без разницы в производительности по сравнению с [!INCLUDE[prod_short](includes/prod_short.md)], запущенным в браузере.
- Приложение открывается в отдельном окне, независимо от окон браузера. Эта функция упрощает поиск при запуске большого количества приложений или вкладок браузера.
- Если у вас несколько сред Business Central (только в Интернете), вы можете установить приложение отдельно для каждой среды.

     Когда вы открываете приложение для определенной среды, имя среды включается в заголовок окна. При работе с несколькими средами [!INCLUDE[prod_short](includes/prod_short.md)] каждое окно приложения отображается отдельно. По названию вам будет легче увидеть, какое окно связано с каждой средой.

## <a name="install-the-app-for-business-central-online"></a>Установка приложения Business Central Online

Установить приложение Business Central Online можно двумя способами. Вы можете установить его прямо из браузера или из Microsoft Store. Какой бы подход вы ни использовали, это одно и то же приложение. Разница в том, что установка из браузера позволяет установить приложение для каждой среды, если их несколько.

### <a name="from-microsoft-store"></a>Из Microsoft Store

1. Перейдите в [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=2182870).
2. Выберите **Получить** > **Установить**. 
3. Когда приложение будет установлено, выберите **Открыть**, затем войдите в Business Central.

В следующий раз, когда вы захотите открыть приложение, найдите его в меню **Пуск**.

### <a name="from-the-browser"></a>Из браузера

1. Откройте веб-клиент [!INCLUDE[prod_short](includes/prod_short.md)] в Microsoft Edge или Google Chrome.

2. Если появится страница выбора среды, вы можете сделать одно из двух:

   - Выберите среду и перейдите к следующему шагу, чтобы установить приложение. В этом случае установленное приложение откроет выбранную вами среду.
   - Не выбирайте среду и просто перейдите к следующему шагу, чтобы установить приложение. В этом случае установленное приложение откроет страницу выбора среды, а не конкретную среду.

3. Чтобы установить приложение, в зависимости от вашего браузера выберите ![Значок для установки приложения в Microsoft Edge.](media/ui-edge-install-app-icon.png) **Приложение доступно. Установить Business Central** или ![Значок для установки приложения в Chrome.](media/ui-chrome-install-app-icon.png) **Установить Business Central**, затем **Установить**.

   | Microsoft Edge | Google Chrome |
   |--|--|
   | :::image type="content" source="media/ui-edge-install-app-v2.png" alt-text="иллюстрация кнопки для установки приложения в Microsoft Edge."::: | :::image type="content" source="media/ui-chrome-install-app-v2.png" alt-text="иллюстрация кнопки для установки приложения в Chrome."::: |

  > [!TIP]
  > С Microsoft Edge вы также можете установить приложение, перейдя в меню **Настройки и другое** в браузере, затем выбрав **Приложения** > **Установить этот сайт как приложение** > **Установить**.

После установки приложение появится в меню **Пуск**. Если вы выбрали определенную среду для приложения, имя среды добавляется к имени приложения в меню **Пуск**.

## <a name="install-the-app-for-business-central-on-premises"></a>Установка приложения Business Central локально

Установка классического приложения при использовании локальной версии Business Central в выполняется прямо в браузере, как [описано выше](#from-the-browser). Если у вас только один клиент, просто откройте Business Central в своем браузере и выберите ![Значок для установки приложения в Microsoft Edge.](media/ui-edge-install-app-icon.png) **Приложение доступно. Установить Business Central** или ![Значок для установки приложения в Chrome.](media/ui-chrome-install-app-icon.png) **Установить Business Central**, как показано выше.

Разница есть, если у вас несколько клиентов. В отличие от [!INCLUDE[prod_short](includes/prod_short.md)] Online, где вы можете установить приложение отдельно для разных сред, здесь вы можете установить приложение только для одного клиента. Поэтому перед установкой приложения, если у вас несколько клиентов, обязательно переключитесь на правильный клиент. После установки, когда вы открываете приложение, оно сразу открывает клиента.

> [!IMPORTANT]
> Если вы используете версию Business Central впуска 2021 волны 1 (версия 18) или более раннюю, вы не сможете установить приложение, как описано в этой статье. Вместо этого установите приложение из [Microsoft Store](https://go.microsoft.com/fwlink/?LinkId=734848). Дополнительные сведения и справку об установке этого устаревшего приложения см. в разделе [Подготовка и установка приложения Business Central](/dynamics365/business-central/dev-itpro/deployment/install-business-central-app).

## <a name="see-related-training-at-microsoft-learn"></a>См. соответствующее обучение на странице [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>См. также

[Вопросы и ответы по мобильным приложениям](ui-mobile-faq.yml)  
[Подготовьтесь к ведению бизнеса](ui-get-ready-business.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]