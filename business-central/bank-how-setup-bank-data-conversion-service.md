---
title: Настройка преобразования банковских данных
description: 'Вы можете настроить банковские счета для отслеживания транзакций и импорта или экспорта банковских выписок, таких как Yodlee.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer'
ms.search.form: '304, 20106, 20105, 20100, 20101, 20107, 20109'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension" />Настройка расширения AMC Banking 365 Fundamentals
Глобальный поставщик услуг преобразования платежной информации в любой формат данных, требуемый банком, подключен и готов к включению в [!INCLUDE[prod_short](includes/prod_short.md)]. В [!INCLUDE[prod_short](includes/prod_short.md)] он называется расширением AMC Banking 365 Fundamentals.

Вы можете экспортировать строки платежей со страницы **Журнал платежей** в файл или поток данных, который затем можно передать в банк для автоматической обработки, чтобы не проводить электронные платежи по одному. Дополнительные сведения см. в разделе [Экспорт платежей в банковский файл](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Можно импортировать файлы банковской выписки на страницу **Журнал выверки платежей** с помощью расширения AMC Banking 365 Fundamentals для конвертации файла, полученного от банка, в поток данных, который может импортировать [!INCLUDE[prod_short](includes/prod_short.md)]. Дополнительные сведения см. в разделе [Автоматическое применение платежей и выверка банковских счетов](receivables-apply-payments-auto-reconcile-bank-accounts.md).

В качестве альтернативы импорту банковских выписок с помощью расширения AMC Banking 365 Fundamentals можно использовать службу Envestnet Yodlee Bank Feeds. Дополнительные сведения см. в разделе [Настройка службы Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Для импорта или экспорта банковских файлов следует настроить собственный банковский счет и банковские счета поставщиков. Дополнительные сведения см. в разделе [Настройка банковских счетов](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> Расширение AMC Banking 365 Fundamentals может налагать ограничение на число строк, экспортируемых в одном файле. Если превысить это ограничение, будет выдано сообщение об ошибке. Рекомендуется, чтобы файлы банковских выписок не превышали 1000 строк, поскольку время обработки в расширении AMC Banking 365 Fundamentals может значительно увеличиться.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension" />Как зарегистрировать компанию в расширении AMC Banking 365 Fundamentals
1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Настройка службы преобр. банковских данных**, а затем выберите связанную ссылку.  
2. Откроется страница **Настройка службы преобр. банковских данных** с тремя полями, предварительно заполненными соответствующими URL-адресами поставщика расширения AMC Banking 365 Fundamentals.

    > [!NOTE]  
    >   В демонстрационной базе денных CRONUS International Ltd. поля "Имя пользователя" и "Пароль" предварительно заполняются демонстрационными данными для входа, которые следует заменить фактическими сведениями об организации при регистрации компании в расширении AMC Banking 365 Fundamentals.
3. В поле **URL-адрес регистрации** нажмите кнопку браузера, чтобы открыть страницу регистрации поставщика услуг.  
4. На странице регистрации поставщика службы преобразования банковских данных введите имя пользователя и пароль для подписки организации на обслуживание, а затем пройдите процесс регистрации, как указано поставщиком службы.

    Ваша компания зарегистрирована в расширении AMC Banking 365 Fundamentals. Затем введите имя пользователя и пароль, указанные для службы в связанных полях настройки в [!INCLUDE[prod_short](includes/prod_short.md)].

5. На странице **Настройка службы преобр. банковских данных** в поле **Имя** введите то же значение, которое было введено как имя для входа на странице поставщика услуг на шаге 4.
6. В поле **Пароль** введите то же значение, которое было введено в поле **Пароль** на странице поставщика услуг на шаге 4.

> [!NOTE]  
> Ваши учетные данные автоматически шифруются.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats" />Просмотр или обновление списка поддерживаемых в настоящее время форматов банковских данных
1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Настройка службы преобр. банковских данных**, а затем выберите связанную ссылку.
2. На странице **Настройка службы преобр. банковских данных** выберите **Название банка – Список преобр. данных**, чтобы открыть список наименований банка, представляющих форматы банковских данных, поддерживаемые службой преобразования.
3. На странице **Название банка – Список преобр. данных** выберите **Обновить список названий банков**.

Список форматов банковских данных, поддерживаемых расширением AMC Banking 365 Fundamentals, теперь обновлен. Это список названий банков, отфильтрованный по странам и регионам, которые можно выбрать в поле **Название банка - преобразование данных** страницы **Карточка банковского счета**.

> [!NOTE]  
>   Обновление поддерживаемых форматов банковских данных также происходит при выборе или вводе значения в поле **Название банка - преобразование данных**.

Вы зарегистрированы в расширении AMC Banking 365 Fundamentals. Продолжите для добавления сведений о регистрации в каждый банковский счет, который будет использовать эту службу.

## <a name="see-also" />См. также
[Настройка банковских операций](bank-setup-banking.md)  
[Выверка банковских счетов](bank-manage-bank-accounts.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
