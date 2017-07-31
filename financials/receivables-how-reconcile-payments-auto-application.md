---
title: "Выверка платежей с использованием автоматического применения | Документы Майкрософт"
description: "Описывается использование функции автоматического применения для применения платежей или приходных кассовых ордеров к соответствующим открытым операциям, а также выверка платежей."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b4ff3d64f23a5dfb9800abeedb7374764b060f4d
ms.contentlocale: ru-ru
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reconcile-payments-using-automatic-application"></a>Практическое руководство. Выверка платежей с использованием автоматического применения
В окне **Журнал выверки платежей** определены платежи (входящие или исходящие), которые записаны как транзакции на вашем счете интернет-банка и которые можно применить к соответствующим открытым операциям книги клиентов, поставщиков и банковских счетов. Строки в журнале заполняются путем импорта банковской выписки в виде файла или потока.

Журнал выверки платежей связан с одним банковским счетом в [!INCLUDE[d365fin](includes/d365fin_md.md)], отражающим счет интернет-банка, где записываются транзакции платежей. Если выбрать действие **Учесть платежи и выверить банковский счет**, все открытые операции книги банковских счетов, связанные с примененными операциями книг клиентов или поставщиков, будут закрыты. Это означает, что банковский счет автоматически выверяется по платежам, которые учтены с использованием журнала.

Чтобы импортировать банковские выписки в электронном виде, необходимо сначала включить службу банковских выписок Envestnet Yodlee, а затем связать банковский счет с соответствующим счетом интернет-банка. В результате журнал выверки платежей автоматически обнаружит банковские выписки при выборе действия **Импорт банковских транзакций.**. Кроме того, можно настроить банковский счет на автоматический импорт новых банковских выписок каждый час. Транзакции по платежам, которые уже были учтены как примененные или выверенные, не будут импортированы. Дополнительные сведения см. в разделе [Практическое руководство. Настройка службы банковских выписок Envestnet Yodlee](bank-how-setup-bank-statement-service.md).

С помощью действий **Определить соответствие текста счетам** можно настроить сопоставления между текстом платежей и конкретными дебетовыми, кредитовыми и балансовыми счетами, чтобы такие платежи учитывались на указанных счетах при учете в журнале выверки платежей. См. шаг 8. Дополнительные сведения см. в разделе [Практическое руководство. Сопоставление текста на типовых платежах со счетами для автоматической выверки](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Аналогичная функция существует для выверки избыточных суммы в строках журнала выверки платежей на произвольной основе. Дополнительные сведения см. в разделе [Практическое руководство. Выверка платежей, которые не могут быть применены](receivables-how-reconcile-payments-cannot-apply-auto.md).

Функция **Применить автоматически** используется либо автоматически при импорте банковского файла или потока с транзакциями платежей или при ее активации, чтобы применить платежи к соответствующим открытым операциям на базе сопоставления данных в строке журнала данным в одной или нескольких открытых операций.

В строках журнала, где платеж применяется автоматически к одной или нескольким открытым операциям, поле **Достоверность совпадения** имеет значение от "Низкий" до "Высокий", что обозначает качество соответствия данных, на основе которого осуществляется предложенное применение платежа. Кроме того, в поля **Тип счета** и **Номер счета** подставляется информация о клиенте или поставщике, к которым был применен платеж. Если настроено сопоставление текст-счет, автоматическое применение может выдать значение с уровнем соответствия **Высокий - Сопоставление текста со счетами**.

Для каждой строки журнала, представляющей платеж, в окне **Журнал выверки платежей** можно открыть окно **Применение платежа**, чтобы просмотреть все открытые операции кандидатов для платежа и подробные сведения о сопоставлении данных, на котором основано применение платежа, для каждой операции. Здесь можно вручную применить платежи или повторно применить платежи, которые были применены автоматически к неверной операции. Дополнительные сведения см. в разделе [Практическое руководство. Проверка или применение платежей после автоматического применения](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
>   Можно начать импорт банковских транзакций одновременно с открытием окна **Журнал выверки платежей** для существующего журнала выверки платежей в окне **Журналы выверки платежей**. В следующей процедуре описан импорт банковских транзакций в окно **Журнал выверки платежей** после создания нового журнала.

## <a name="to-reconcile-payments-using-automatic-application"></a>Выверка платежей с использованием автоматического применения
1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журналы выверки платежей**, а затем выберите связанную ссылку.
2. Для работы в новом журнале выверки платежей выберите действие **Создать журнал**.
3. В окне **Список банковских счетов платежа** выберите банковский счет, для которого вы хотите выверить платежи, а затем нажмите кнопку **ОК**.
   Откроется окно **Журнал выверки платежей**, подготовленное для выбранного банковского счета.
4. Выберите действие **Импорт банковских транзакций**.
   Если банковский счет для выбранного журнала не настроен для импорта банковских транзакций, откроется диалоговое окно, в котором можно будет заполнить соответствующие поля.
5. В окне **Выберите файл для импорта** выберите файл, содержащий банковские транзакции для платежей, которые нужно выверить, и выберите кнопку **Открыть**.  
6. Если служба банковских выписок включена, в окне **Фильтр банковских выписок**, которое откроется автоматически, укажите интервал дат для импорта банковских выписок.

    Окно **Журнал выверки платежей** заполняется строками для платежей, представляющих банковские транзакции в импортируемой банковской выписке.

    В строках платежей, автоматически примененных к соответствующим открытым операциям, поле **Достоверной совпадения** имеет значение от **Низкий** до **Высокий**, что обозначает качество соответствия данных, на основе которого осуществляется предложенное применение платежа. Кроме того, в поля **Тип счета** и **Номер счета** подставляется информация о клиенте или поставщике, к которым был применен платеж.
7. Выберите строку журнала, а затем выберите действие **Применить вручную**, чтобы проверить, повторно применить или применить платеж вручную в окне **Применение платежа**. Дополнительные сведения см. в разделе [Практическое руководство. Проверка или применение платежей после автоматического применения](receivables-how-review-apply-payments-auto-application.md).

    По завершении применения вручную в поле **Достоверность совпадения** в строке журнала, обработанной вручную, содержится значение **Принято**.
8. Выберите непримененную строку журнала для типового приходного или расходного кассового ордера, например покупки бензина для автомобиля, а выберите **Определить соответствие текста счетам**. Дополнительные сведения см. в разделе [Практическое руководство. Сопоставление текста на типовых платежах со счетами для автоматической выверки](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).
9. Завершив сопоставление текста платежей и счетов, выберите действие **Применить вручную**.
10. Если все платежи в строках журнала применены правильно или для них задан прямой учет, выберите действие **Учесть**.

При учете журнала выверки платежей примененные открытые операции закрываются, а соответствующие счета клиентов, поставщиков или ГК обновляются. Платежи в строках журнала основаны на сопоставлении текст-счет, указанные счета клиента, поставщика и ГК обновляются. Для всех строк журнала создаются записи журнала банковского счета. Если выбрать действие **Учесть платежи и выверить банковский счет**, все открытые операции книги банковских счетов, связанные с примененными операциями книг клиентов или поставщиков, будут закрыты. Это означает, что банковский счет автоматически выверяется по платежам, которые учтены с использованием журнала.

Можно сравнить значение в поле **Сальдо на банковском счету после учета** со значением в поле **Конечное сальдо выписки**, чтобы отследить, когда выполняется выверка банковского счета на основе учитываемых платежей.

> [!NOTE]  
>   Если выверять банковский счет из окна **Журнал выверки платежей** не требуется, вы должны использовать окно **Выверка банковского счета**. Дополнительные сведения см. в разделе [Выверка банковских счетов по-отдельности](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>См. также
[Управление дебиторской задолженностью](receivables-manage-receivables.md)  
[Продажи](sales-manage-sales.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
