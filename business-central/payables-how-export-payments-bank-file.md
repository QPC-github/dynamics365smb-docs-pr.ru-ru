---
title: "Экспорт платежей в файл электронного платежа | Документы Майкрософт"
description: "Чтобы осуществить платеж поставщику, необходимо включить службу конвертации банковских данных, экспортировать файл банка и загрузить этот файл в электронный банк для перевода средств."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 88406936af640a2ec31f099fcae8bf039b64ecf3
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="export-payments-to-a-bank-file"></a>Экспорт платежей в банковский файл
Когда все будет готово для осуществления платежей поставщикам или возмещения расходов ваших сотрудников, можно экспортировать файл со сведениями о платежах в строках в окне **Журнал платежей**. Затем можно отправить файл в банк для обработки соответствующих денежных переводов.

В общей версии [!INCLUDE[d365fin](includes/d365fin_md.md)] настраивается и подключается глобальный поставщик услуг для преобразования банковских данных в любой формат файла, требуемый банком. В версиях для Северной Америки одну службу можно использовать для отправки файлов платежей как электронного платежа (EFT), однако процесс немного отличается. См. шаг 6 в разделе "Экспорт платежей в банковский файл".    

> [!NOTE]  
>   Прежде чем можно будет экспортировать файлы платежей из журнала платежей, следует указать электронный формат для используемого банковского счета и включить службу конвертации банковских данных. Дополнительные сведения см. в разделах [Настройка банковских счетов](bank-how-setup-bank-accounts.md) и [Настройка службы конвертации банковских данных](bank-how-setup-bank-data-conversion-service.md). Кроме того, необходимо установить флажок **Разрешить экспорт платежей** в окне **Разделы финансового журнала**. Дополнительные сведения см. в разделе [Работа с финансовыми журналами](ui-work-general-journals.md).  

Окно **Регистры кредитовых переводов** служит для просмотра файлов платежей, которые были экспортированы из журнала платежей. Из этого окна можно также повторно экспортировать файлы платежей в случае технических ошибок или изменения файлов. Однако обратите внимание, что файлы EFT не отображаются в этом окне и не могут быть экспортированы повторно.  

## <a name="to-export-payments-to-a-bank-file"></a>Экспорт платежей в файл банка
1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журналы платежей**, а затем выберите связанную ссылку.
2. Заполните строки журнала платежей, например с помощью функции **Предлож. оплаты поставщикам**. Дополнительные сведения см. в разделе [Предложение оплаты поставщикам](payables-how-suggest-vendor-payments.md).
3. Заполните поля в строках журнала платежей по мере необходимости. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Если используется EFT, необходимо выбрать **Электронный платеж** или **Электронный платеж IAT** в поле **Тип банковского платежа**. Различные службы экспорта файлов и их форматы требуют различных значений настройки в окнах **Карточка банковского счета** и **Карточка банк. счета поставщика**. Вы получите сообщения о неверных или отсутствующих значениях настройки при попытке экспорта файла.

4. После того как будут заполнены все строки журнала платежей, выберите действие **Экспорт**.
5. В окне **Экспорт электронных платежей** заполните требуемые поля.

    Все сообщения об ошибках будут отображаться на информационной панели **Ошибки файла платежей**, на которой также можно выбрать сообщение об ошибке, чтобы просмотреть подробные сведения. Перед экспортом файла оплаты необходимо устранить все ошибки.

    > [!TIP]  
    >   При использовании службы преобразования банковских данных часто появляется сообщение об ошибке, в котором говорится, что длина номера банковского счета не соответствует правилам банка. Чтобы избежать этой ошибки или устранить ее, необходимо удалить значение в поле **IBAN** в окне **Карточка банковского счета**, а затем в поле **Номер банковского счета** ввести номер банковского счета в формате, требуемом вашим банком.

6. В окне **Сохранить как** укажите папку, в которую экспортируется файл, а затем выберите **Сохранить**.

    > [!NOTE]  
    >   Если используется EFT, сохраните полученную форму предъявления к оплате поставщика как документ Word или выберите его отправку по электронной почте напрямую поставщику. Платежи добавлены в окне **Создать файл EFT**, в котором можно создать несколько платежных поручений одновременно, чтобы сократить затраты на передачу. Дополнительные сведения см. в следующих шагах.
7. В окне **Журнал платежей** выберите действие **Создать файл EFT**.

    В окне **Создать файл EFT** все платежи, настроенные для EFT, экспортированные из журнала платежей для указанного банковского счета, но еще не созданные, перечисляются на экспресс-вкладке **Строки**.
8. Выберите действие **Создать файл EFT** для экспорта одного файла для всех платежей EFT.
9. В окне **Сохранить как** укажите папку, в которую экспортируется файл, а затем выберите **Сохранить**.

Файл банковских платежей экспортируется в указанное расположение, откуда его можно отправить на электронный банковский счет и осуществить фактические платежи. Затем можно учесть экспортированные строки журнала платежей.

## <a name="to-export-payments-that-represent-customer-refunds"></a>Экспорт платежей, представляющих возмещения клиентам
Ниже описывается обходной путь для экспорта электронных платежей возмещения.

> [!CAUTION]  
>   Итоговые строки журнала платежей невозможно учесть, удалить или аннулировать.
1. Настройте клиента как поставщика. Например, назовем его "Клиент X для возмещений". Дополнительные сведения см. в разделе [Регистрация новых поставщиков](purchasing-how-register-new-vendors.md).
2. В строке журнала платежей для клиента установите в поле **Тип счета** значение **Клиент**, а в поле **Тип документа** — **Возмещение**.
3. Выполните обычные шаги для экспорта платежей, как описано в разделе "Экспорт платежей в банковский файл".

## <a name="to-plan-when-to-post-exported-payments"></a>Планирование учета экспортированных платежей
Если не требуется учитывать строку журнала платежей для экспортированного платежа, например потому что ожидается подтверждение обработки транзакции банком, можно просто удалить строку журнала. Впоследствии при создании строки журнала платежей, чтобы оплатить оставшуюся сумму по счету, в поле **Общая сумма экспорта** можно просмотреть уже экспортированную сумму платежа. Кроме того, чтобы просмотреть подробные сведения об общей сумме экспорта, можно нажать кнопку **Операции регистров кредитных переводов** для просмотра подробных сведений об экспортированных файлах платежей.

Если вы используете процесс, в котором платежи не учитываются до получения от банка подтверждения о том, что они были обработаны, это можно реализовать двумя способами.

* В журнале платежей с предложенными строками платежей можно выполнить сортировку по столбцу **Экспортировано в файл платежей** или **Общая сумма экспорта**, а затем удалить предложения оплаты для открытых счетов, по которым уже выполнены платежи и для которых не требуется выполнять платежи.
* В окне **Предлож. оплаты поставщикам**, в котором указывается, какие платежи следует вставить в журнал платежей, можно установить флажок **Пропустить экспортированные платежи**, если не требуется вставлять строки журнала для платежей, которые уже были экспортированы.

Чтобы просмотреть сведения об экспортированных платежах, выберите действие **История экспортированных платежей**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Повторный экспорт платежей в банковский файл
Можно повторно экспортировать файлы платежей из окна **Регистры кредитовых переводов**. Прежде чем удалить или учесть строки журнала платежей, также можно повторно экспортировать файл платежей из окна **Журнал платежей**, выполнив повторный экспорт. Если строки журнала платежей удалены или учтены после их экспорта, можно повторно экспортировать тот же файл платежей из окна **Регистры кредитовых переводов**. Выберите строку для пакета кредитовых переводов, которые необходимо повторно экспортировать, а затем выберите действие **Повторный экспорт платежей в файл**.

> [!NOTE]  
>   Экспортированные файлы EFT не отображаются в окне **Регистры кредитовых переводов** и не могут быть экспортированы повторно.

1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Регистры кредитовых переводов**, а затем выберите связанную ссылку.
2. Выберите экспорт платежей, который необходимо экспортировать повторно, и выберите действие **Повторный экспорт платежа в файл**.

## <a name="see-also"></a>См. также
[Кредиторская задолженность](payables-manage-payables.md)  
[Настройка покупки](purchasing-setup-purchasing.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
