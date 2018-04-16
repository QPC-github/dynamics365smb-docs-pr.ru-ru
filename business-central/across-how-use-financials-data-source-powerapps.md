---
title: "Использование данных для создания приложения | Microsoft Docs"
description: "Данные Financials можно сделать доступными в качестве источника данных и указать URL-адрес OData ваших веб-служб для создания бизнес-приложения с помощью PowerApps."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 0e6310e9789e8a0f2ceaed44f1209cdcf425ef1e
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-to-your-financials-data-to-build-a-business-app-using-powerapps"></a>Подключение к данным Financials для создания бизнес-приложения с помощью PowerApps
Данные [!INCLUDE[d365fin](includes/d365fin_md.md)] можно сделать доступными как источник данных в PowerApps.  

> [!NOTE]  
>   Вы должны иметь допустимую учетную запись в [!INCLUDE[d365fin](includes/d365fin_md.md)] и в PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Добавление [!INCLUDE[d365fin](includes/d365fin_md.md)] как источника данных в PowerApps
1. В браузере перейдите к [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) и выполните вход.
2. В левой области навигации выберите **Новое приложение**.
3. Выберите редактор: PowerApps Studio для Windows или PowerApps Studio для сети.

   PowerApps Studio для Windows — это приложение рабочего стола, используемое для создания и публикации PowerApps. PowerApps Studio для сети — это веб-решение, используемое для создания и публикации PowerApps.
4. Следующий шаг создания PowerApp — выбор данных. Щелкните значок стрелки, а затем выберите параметр **Новое подключение** в левом верхнем углу страницы.
5. В списке доступных подключений выберите **Dynamics 365 Business Central**.
6. PowerApps отобразит страницу подключения с запросом на ввод информации, необходимой для подключения к данным [!INCLUDE[d365fin](includes/d365fin_md.md)]. Чтобы подключиться, следует указать URL-адрес OData, имя пользователя, пароль и название организации.

   Для параметра *URL-адрес OData* можно скопировать URL-адрес OData V4 любой из веб-служб, перечисленных на странице **Веб-службы** в [!INCLUDE[d365fin](includes/d365fin_md.md)], например `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Для параметра *Название организации* используйте название, которое отображается в поле **Имя** в окне **Информация об организации** в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Если [!INCLUDE[d365fin](includes/d365fin_md.md)] содержит несколько организаций, выберите соответствующее название организации из списка в окне **Организации**. В обоих случаях убедитесь, что название, указываемое в мастере PowerApps точно соответствует тексту, отображаемому в [!INCLUDE[d365fin](includes/d365fin_md.md)], например `My Company`.

   В качестве имени пользователя и пароля используйте имя и ключ доступа веб-службы, определенные для учетной записи в окне **Пользователи** в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Например, ваше имя пользователя — *ADMIN*, а ключ доступа веб-службы, который используется как пароль, — *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Нажмите кнопку **Подключение**, чтобы продолжить. PowerApps отобразит набор данных по умолчанию для [!INCLUDE[d365fin](includes/d365fin_md.md)]. Выберите набор данных **По умолчанию**.

   PowerApps отобразит список таблиц, доступных для [!INCLUDE[d365fin](includes/d365fin_md.md)]. Эти таблицы или конечные точки представляют все веб-службы, которые вы опубликовали из [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Либо создайте новый URL-адрес веб-службы в [!INCLUDE[d365fin](includes/d365fin_md.md)], используя действие **Создать набор данных** на странице **Веб-службы** с помощью руководства по сопровождаемой настройке **Настройка отчетов** либо используя действие **Изменить в Excel** в любом списке.
8. Выберите таблицу, которая будет использоваться для PowerApp, а затем нажмите кнопку **Подключиться**.
9. Повторите предыдущие шаги для добавления дополнительных данных [!INCLUDE[d365fin](includes/d365fin_md.md)] в модель данных Power BI.

   > [!NOTE]  
   >    После успешного подключения к [!INCLUDE[d365fin](includes/d365fin_md.md)] вводить URL-адрес OData, имя пользователя или пароль повторно не требуется.

На этом шаге вы успешно подключились с данным Business Central и готовы начать создание вашего приложения PowerApp. Дополнительные сведения см. в разделе [Документация PowerApps](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>См. также
[Приступая к работе](product-get-started.md)  
[Импорт бизнес-данных из других финансовых систем](upload-data.md)  
[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Финансы](finance.md)  
