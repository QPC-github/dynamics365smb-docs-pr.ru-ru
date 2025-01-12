---
title: Настройка валют
description: 'Необходимо настроить каждую валюту, если вы покупаете или продаете товары за валюты, отличные от вашей местной валюты, или записываете транзакции ГК в разных валютах.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="set-up-currencies" />Настройка валют

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Используйте внешнюю службу для получения самых актуальных валютных курсов в списке **Валюты**. Дополнительные сведения см. в разделе [Настройка служб валютных курсов](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="a-namecurracurrencies" /><a name="curr"></a>Валюты

В следующей таблице описываются другие поля в списке **Валюты**.

|Поле|Описание|  
|---------------------------------|---------------------------------------|  
|**Код**|Идентификатор валюты.|
|**Описание**|Свободное текстовое описание валюты.|
|**Код ISO**|Международный трехбуквенный код валюты, определенный в ISO 4217.|
|**Цифровой код ISO**|Международный числовой код валюты, определенный в ISO 4217.|
|**Дата валютного курса**|Самая последняя дата фактического обменного курса.|
|**Валюта ЕС**|Указывает, является ли валюта валютой ЕС (Экономического и валютного союза), например евро.|
|**Счет реализованной прибыли**|Счет, на котором будет учитываться фактическая прибыль при получении платежей по дебиторской задолженности или регистрации фактического курса валюты по платежам в счет кредиторской задолженности. Для примера валютной проводки дебиторской задолженности см. пример под этой таблицей. |
|**Счет реализованного убытка**|Счет, на котором будет учитываться фактический убыток при получении платежей по дебиторской задолженности или регистрации фактического курса валюты по платежам в счет кредиторской задолженности. Для примера валютной проводки дебиторской задолженности см. пример под этой таблицей. |
|**Счет нереализованной прибыли**|Счет, на котором будет учтена теоретическая прибыль при корректировке валюты.|
|**Нереализованный убыток**|Счет, на котором будет учтен теоретический убыток при корректировке валюты.|
|**Точность округления суммы**|Некоторые валюты имеют другие форматы для сумм счетов, чем те, которые определены на странице **Настройка ГК**. Если вы измените точность округления сумм для валюты, все суммы счетов в этой валюте будут округлены с обновленной точностью.|
|**Десятичные знаки в сумме**|Некоторые валюты имеют другие форматы для сумм счетов, чем те, которые определены на странице **Настройка ГК**. Если вы измените десятичные знаки в сумме для валюты, все суммы счетов в этой валюте будут округлены с обновленным десятичными знаками.|
|**Тип округления счета**|Задает метод, который следует использовать, если суммы должны быть округлены. Варианты **Ближайшее**, **Вверх** и **Вниз**.|
|**Точность округления цены единицы**|Некоторые валюты имеют другие форматы для сумм единицы, чем те, которые определены на странице **Настройка ГК**. Если вы измените точность округления единиц для валюты, все суммы единиц в этой валюте будут округлены с обновленной точностью.|
|**Десятичные знаки в цене единицы**|Некоторые валюты имеют другие форматы для сумм единицы, чем те, которые определены на странице **Настройка ГК**. Если вы измените десятичные знаки в сумме единицы для валюты, все суммы единиц в этой валюте будут округлены с обновленным десятичными знаками.|
|**Точность округления при применении**|Определяет размер интервала, разрешенного как разница округления при взаимодействии операций в разных валютах.|
|**Округление при конвертации в МВ Дебетовый счет**|Определяет сведения о преобразовании, которые, помимо прочего, должны содержать дебетовый счет, если необходимо при помощи действия **Вставить строки округл. для конвертации в МВ** ввести в финансовые журналы строки коррекции для разниц округления.|
|**Округление при конвертации в МВ Кредитовый счет**|Определяет сведения о преобразовании, которые, помимо прочего, должны содержать кредитовый счет, если необходимо при помощи действия **Вставить строки округл. для конвертации в МВ** ввести в финансовые журналы строки коррекции для разниц округления.|
|**Дата последней коррекции**|Дата последней валютной корректировки.|
|**Дата последнего изменения**|Дата изменения настройки валюты.|
|**Отклонение в оплате %**|Максимальный % отклонения в оплате для этой валюты. Для получения дополнительной информации см. [Отклонение в оплате и отклонение от скидки оплаты](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Макс. сумма отклонения оплаты**|Максимальная сумма отклонения в оплате для этой валюты. Для получения дополнительной информации см. [Отклонение в оплате и отклонение от скидки оплаты](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Коэффициент курса валюты**|Задает отношение между валютой и местной валютой с помощью фактического курса валюты.|
|**Счет ГК реализ. прибыли**|Определяет счет ГК, на который будет учитываться прибыль, получаемая при корректировке валютных курсов между местной валютой (МВ) и дополнительной отчетной валютой. Прибыли по курсовым разницам рассчитывается при запуске пакетного задания "Корректировка валютных курсов" для корректировки счетов главной книги. По умолчанию это поле может не отображаться. Его можно получить, настроив страницу.|
|**Счет ГК реализованного убытка**|Определяет счет ГК, на который будут учитываться убытки, получаемые при корректировке валютных курсов между местной валютой (МВ) и дополнительной отчетной валютой. Прибыли по курсовым разницам рассчитывается при запуске пакетного задания "Корректировка валютных курсов" для корректировки счетов главной книги. По умолчанию это поле может не отображаться. Его можно получить, настроив страницу.|
|**Счет остаточной прибыли**|Задает счет ГК, который используется для учета сумм остаточной прибыли (разницы от округления), когда в области приложения главной книги используется дополнительная валюта отчетности. По умолчанию это поле может не отображаться. Его можно получить, настроив страницу.|
|**Счет остаточных убытков**|Задает счет ГК, который используется для учета сумм остаточного убытка (разницы от округления), когда в области приложения главной книги используется дополнительная валюта отчетности. По умолчанию это поле может не отображаться. Его можно получить, настроив страницу.|
|**Максимальная разрешенная разница НДС**|Максимально допустимая сумма разницы по НДС в этой валюте. Дополнительно см. в разделе [Ручная корректировка сумм НДС в документах продаж и покупок](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). По умолчанию это поле может не отображаться. Его можно получить, настроив страницу.|
|**Тип округления НДС**|Задает метод округления для корректировки сумм НДС вручную в документах купли-продажи. По умолчанию это поле может не отображаться. Его можно получить, настроив страницу.|

### <a name="available-currency-functions" />Доступные валютные функции

В следующей таблице описаны основные действия на странице **Валюты**.  

|Меню|Действие|Описание|
|-------------|--------------|------------------------------|
|**Обработать**|**Предложить счета**|Используйте счета в других валютах. Будут вставлены наиболее часто используемые учетные записи.|
||**Изменение отклонения в оплате**|Изменение максимального отклонения в оплате и/или отклонения в оплате в процентах и фильтров по валюте. Для получения дополнительной информации см. [Отклонение в оплате и отклонение от скидки оплаты](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Валютные курсы**|Просмотр обновленных валютных курсов для используемых валют.|
||**Коррекция курс. разниц**|Корректировка главной книги, а также бухгалтерских записей клиента, поставщика и банка, чтобы в них были отражены последние данные об изменении баланса, если со времени учета операций валютный курс изменился.|
||**Регистр коррекции валютных курсов**|Просмотрите результаты выполнения пакетного задания **Корректировка валютных курсов**. Строка создаётся для каждой валюты или для каждой комбинации валюты и учётной группы, которые включены в коррекцию.|
|**Служба валютных курсов**|**Службы валютных курсов**|Просмотр или изменение параметров служб, которые настроены для получения обновленных валютных курсов при выборе действия **Обновить валютные курсы**.|
||**Обновить валютные курсы**|Получение последних валютных курсов от поставщика службы.|
|**Отчеты**|**Сальдо в иностранной валюте**|Представление балансов для всех клиентов и поставщиков в иностранных и местной валютах (МВ). В отчете показывается два баланса в МВ. Одно значение — сальдо в иностранной валюте, преобразованное в МВ путем использования валютного курса на дату транзакции. Другое значение — сальдо в иностранной валюте, преобразованное в МВ путем использования валютного курса рабочей даты.|

## <a name="lcy-and-other-currencies" />Местная и другие валюты

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## <a name="rounding-currencies" />Валюты для округления

Для управления валютами, в значениях которых не используются десятичные цифры, а также во избежание использования десятичных цифр в значениях в иностранной валюте, можно использовать две функции округления.

- Округление цены  

- Округление суммы  

Эти функции могут использоваться как сами по себе, так и вместе. Кроме того, их можно использовать в сочетании с функцией округления счетов.

В отличии от функций округления счетов функции округления сумм и цен влияют только на суммы в иностранной валюте, а не на соответствующие суммы в рублях. Их использование не приводит к учету по счетам главной книги. Соответственно, счета главной книги можно не указывать ни в учетных группах, ни где бы то ни было.

### <a name="unit-amount-rounding" />Округление цены

Функция округления цены управляет округлением цен продажи для товаров и ресурсов в иностранных валютах в строках продажи и покупки. Для каждой валюты необходимо указать правило в списке **Валюты** в поле **Точность округления цены**.

Функция округления цены используется автоматически каждый раз при вводе номера товара или ресурса в строку продажи. Если счет предназначен для клиента с кодом валют, цена товара или ресурса переводится в валюту клиента. Цена округляется согласно точности округления цены для данной валюты.

### <a name="amount-rounding" />Округление суммы

Функция округления сумм управляет округлением сумм в иностранной валюте в строках финансового журнала, строках продажи и покупки. Для каждой валюты необходимо указать правило в списке **Валюты** в поле **Точность округления суммы**.

Суммы в иностранных валютах округляются при заполнении и учете строк финансового журнала, строк продажи и покупки.

## <a name="exchange-rates" />Валютные курсы

Валютные курсы можно задать для каждой иностранной валюты, указав при этом даты, при наступлении которых они вступят в силу. Например, для каждой иностранной валюты можно задать валютный курс на день, месяц или квартал.

Для получения в дальнейшем сведений об исторических валютных курсах их можно сохранить на странице **Валютные курсы**. Для обновления валютных курсов нажмите кнопку **Обновить валютные курсы** для получения самых актуальных курсов от внешнего поставщика услуги.

## <a name="general-ledger-accounts" />Счета ГК

Коды валют нельзя связать со счетами главной книги, поскольку суммы в счетах главной книги задаются в рублях. При наличии банковской ссуды в долларах США и зачислении депозитов на банковский счет в шведских кронах эти счета можно отслеживать, указав в настройках банковских счетов в доллары США и шведские кроны. Учетные группы используются для того, чтобы связать банковские счета с соответствующими счетами главной книги. В Главной книге величина сумм отражается в рублях.

В строке финансового журнала можно ввести код валюты и учесть ее в счете главной книги. Для конвертирования суммы в рубли перед ее учетом в счете главной книги будет использован соответствующий валютный курс.  

## <a name="example-of-a-receivable-currency-transaction" />Пример транзакции с валютой дебиторской задолженности

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-related-microsoft-trainingtrainingmodulescurrencies-exchange-rates-dynamics-365-business-central" />См. соответствующее [обучение Microsoft](/training/modules/currencies-exchange-rates-dynamics-365-business-central/)

## <a name="see-also" />См. также

[Обновление валютных курсов](finance-how-update-currencies.md)  
[Настройка дополнительной отчетной валюты](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
