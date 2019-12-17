---
title: Использование расширения AMC Banking 365 Fundamentals | Документы Microsoft
description: Легко обменивайтесь данными с вашими банками, преобразовывая данные в нужный им формат.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: bank, format, data
ms.date: 10/14/2019
ms.author: bholtorf
ms.openlocfilehash: 9c9d927fb13d68c195bd457eb6bd2cbbfe078ea2
ms.sourcegitcommit: 86498fe4326b9ce26cc31e8645db27570d13bdf9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2767542"
---
# <a name="using-the-amc-banking-365-fundamentals-extension"></a>Использование расширения AMC Banking 365 Fundamentals
Расширение AMC Banking 365 Fundsmentals упрощает и делает более точной отправку данных в ваши банки. Расширение подключает [!INCLUDE[d365fin](includes/d365fin_md.md)] к службе AMC Banking 365 Fundamentals для Microsoft Dynamics 365 Business Central, которая может конвертировать банковские данные из [!INCLUDE[d365fin](includes/d365fin_md.md)] в форматы, которые требуются более чем 600 банками по всему миру. Например, это облегчает перевод платежей и кредитов поставщикам путем ввода платежей в [!INCLUDE[d365fin](includes/d365fin_md.md)], а затем отправки их в ваш банк. Форматы также могут упростить процессы выверки банковских счетов. Для получения дополнительной информации см. раздел [AMC Banking для Microsoft Dynamics 365 Business Central](https://amcbanking.com/landing365bc/help),

> [!Note]
> AMC Banking имеет встроенные дополнительные расширения, которые работают с [!INCLUDE[d365fin](includes/d365fin_md.md)]. В этом разделе описывается только расширение Fundamentals.

## <a name="using-our-demonstration-account"></a>Использование нашей демонстрационной учетной записи
[!INCLUDE[d365fin](includes/d365fin_md.md)] поставляется с демонстрационной учетной записью, которая позволяет вам попробовать расширение AMC Banking 365 Fundamentals. Мы предоставляем настройки по умолчанию для подключения к AMC Banking с указанием банковских счетов, из которых требуется получать данные, в [!INCLUDE[d365fin](includes/d365fin_md.md)], плюс несколько определений обмена данными. Вы можете просмотреть настройки подключения на странице **Настройка AMC Banking**. Для банковских счетов расширение применяет значения в полях **Название банка**, **Номера сообщ. кред. переводов**, **Формат импорта банковской выписки** и **Формат экспорта платежей** на карточках банковских счетов.

Мы предоставляем настройки, но чтобы опробовать расширение, вы должны запустить мастер настройки, чтобы применить их. Чтобы запустить мастер, на странице **Настройка AMC Banking** выберите действие **Мастер настройки**.

> [!Note]
> На демонстрационной учетной записи есть некоторые ограничения. Например, при преобразовании платежей сумма в преобразованном файле не будет соответствовать фактической сумме. Вместо этого сумма всегда будет равна пяти единицами валюты, которую вы используете для платежей.  

## <a name="setting-up-the-extension"></a>Настройка расширения
Начало работы с расширением включает в себя всего несколько простых шагов, и мастер настройки установит соединение и включит расширение. Руководство будет выполнять такие вещи, как установка определений обмена данными для настроек экспорта/импорта банковских выписок и инициирование серий номеров, используемых для сообщений о кредитных переводах.  

### <a name="to-set-up-the-required-permission-sets"></a>Настройка необходимых наборов разрешений
Прежде чем люди смогут использовать это расширение, ваш администратор должен скопировать следующие наборы разрешений, отредактировать их, а затем назначить новые наборы разрешений пользователям вместо оригинальных:

* **D365 Basic**
* **D365 Team Member**
* **D365 Read**
* **IntelligentCloudBC**

Дополнительные сведения см. в разделе [Копирование набора разрешений](ui-define-granular-permissions.md#to-copy-a-permission-set).

Для каждого нового набора разрешений предоставьте только разрешение **Чтение** для элемента **Таблица настройки AMC Banking (20101)**. Дополнительные сведения см. в разделе [Создание и изменение разрешений вручную](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-connect-the-extension-to-amc-banking"></a>Чтобы подключить расширение к AMC Banking
1. Получить модуль и план обслуживания для AMC Banking. Для этого посетите страницу [Лицензия AMC](https://license.amcbanking.com/register).
2. В [!INCLUDE[d365fin](includes/d365fin_md.md)] выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка AMC Banking**, затем выберите соответствующую ссылку.  
3. На странице **Настройка AMC Banking** выберите действие **Мастер настройки**.
4. Выполните шаги облегчить в мастере настройки.

### <a name="to-connect-bank-accounts-to-the-extension"></a>Подключение банковских счетов к расширению
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Банковские счета**, затем выберите соответствующую ссылку.
2. Откройте карту для банковского счета, который вы хотите подключить к услуге.
3. в поле **Название банка** выберите формат, который требуется вашему банку.  

   Форматы фильтруются, чтобы показать только те из них, которые имеют отношение к стране/региону, указанному для банковского счета.
4. В поле **Номера сообщ. кред. переводов** выберите номер серии для сообщений, сопровождающих платежи.
5. В полях **Формат импорта банковской выписки** и **Формат экспорта платежей** выберите определения обмена данными, которые требуются вашему банку.

## <a name="using-the-extension"></a>Использование расширения
Использование этого расширения — это всего лишь вопрос экспорта данных на странице **Журналы платежей**, а затем отправки его в веб-службу вашего банка. Дополнительные сведения см. в разделе [Выполнение платежей с помощью обработки данных банка или кредитового перевода SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!Note]
> Вы должны заполнить поля **SWIFT-код** и **IBAN** для каждого банковского счета.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>Экспорт данных и отправка их в ваш банк
> [!CAUTION]  
>  При экспорте данных с помощью расширения AMC Banking 365 Fundamentals некоторые бизнес-данные станут доступны поставщику службы. Поставщик услуг AMC Consult A/S отвечает за конфиденциальность этих данных. Дополнительные сведения см. в разделе [Политика конфиденциальности AMC](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Журналы платежей**, затем выберите соответствующую ссылку.
2. Создайте строки журнала, которые нужно экспортировать.  

   > [!Note]
   > Для каждой строки не забудьте выбрать **Электронный платеж** в поле **Тип банковского платежа**.
3. Выберите действие **Экспорт**.

### <a name="to-import-and-apply-the-converted-file"></a>Импорт и применение преобразованного файла
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Журнал выверки платежей**, затем выберите соответствующую ссылку.
2. Выберите действие **Импорт банковских транзакций**, затем выберите преобразованный файл.  

   [!INCLUDE[d365fin](includes/d365fin_md.md)] создаст новый журнал выверки платежей, содержащий данные в файле. Дополнительные сведения см. в разделе [Автоматическое применение платежей и выверка банковских счетов](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>См. также
[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью расширений](ui-extensions.md)  
[Приступая к работе](product-get-started.md)