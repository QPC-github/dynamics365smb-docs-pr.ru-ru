---
title: Регистрация специальных цен покупки и скидок
description: Вы можете задать соглашения об альтернативных ценах и скидках и применять их к документам покупки для поставщиков.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '26, 1346, 7012, 7014, 7017, 7018, 7189, 7190, 9307'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="record-special-purchase-prices-and-discounts" />Регистрация специальных цен покупки и скидок

> [!NOTE]
> Во 2-й волне выпуска 2020 года мы выпустили оптимизированные процессы для настройки цен и скидок и управления ими. Если вы новый клиент, использующий эту версию, вы используете новую версию. Если вы уже являетесь клиентом, то используете ли вы новый интерфейс, зависит от того, включил ли ваш администратор обновление функции **Новые возможности ценообразования для продажи** в **Управление функциями**. Для получения дополнительной информации см. [Раннее включение новых функций](/dynamics365/business-central/dev-itpro/administration/feature-management).

Необходимо определить соглашения о скидках и ценах, которые будут применяться при покупке у различных поставщиков, чтобы к документам покупки, созданным для поставщика, применялись согласованные правила и значения.

После регистрации специальных цен и скидок по строке для покупок и продаж [!INCLUDE[prod_short](includes/prod_short.md)] гарантирует, что ваша прибыль от торговли товаром будет всегда оптимальна, автоматически рассчитывая наилучшую цену в документах продажи и покупки и в строках журнала товаров и работ. Дополнительные сведения см. в разделе [Расчет лучшей цены](purchasing-how-record-purchase-price-discount-payment-agreements.md#best-price-calculation).

В отношении цен, вы можете вводить в строки покупок определенную цену для определенного сочетания поставщика, минимального количества, единицы измерения или даты начала/окончания.

В отношении скидок, вы можете настроить и использовать два типа скидок покупки:

| Тип скидки | Описание |
| --- | --- |
| **Скидки строки покупки** |Сумма скидки, которая вводится в строки покупки для определенного сочетания поставщика, минимального количества, единицы измерения или даты начала/окончания. Этот тип работает так же, как и для цен покупки. |
| **Скидка по счету** |Процентная скидка, которая вычитается из общей суммы документа, если сумма всех строк документа покупки превышает определенный минимум. |

Так как скидки строк покупки и цены покупки зависят от комбинации товара и поставщика, можно также ввести эту конфигурацию из карточки товара, в которой определяются правила и значения. Дополнительные сведения см. в разделе [Регистрация новых товаров](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor" />Настройка специальных цен покупки для поставщика

#### [Текущая версия](#tab/current-experience)

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Поставщики**, а затем выберите связанную ссылку.
2. Откройте соответствующую карточку поставщика и выберите действие **Цены**.
3. Заполните поля в строке по мере необходимости. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Заполните строку для каждой комбинации, для которой поставщик предоставляет скидку строки покупки.

#### [Новая версия](#tab/new-experience)

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Поставщики**, а затем выберите связанную ссылку.
2. Выберите поставщика, затем выберите действие **Прайс-листы продажи**.
3. Выберите **Создать** для создания нового прайс-листа закупок.
4. На экспресс-вкладках **Общее** и **Налог** заполните необходимые поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Чтобы добавить элементы в список, выполните одно из следующих действий:
   * Чтобы добавить много элементов, выберите **Предложить строки**, а затем введите критерии фильтрации, чтобы указать типы добавляемых элементов. При желании вы также можете ввести некоторые дополнительные настройки для номенклатур, относящихся к прайс-листу. Если требуется, это можно изменить позднее.
   * Чтобы скопировать номенклатуры из другого прайс-листа, выберите **Копировать строки**, а затем выберите прайс-лист для копирования.
   * Чтобы добавить элементы вручную, в сетке в поле **Тип продукта** выберите тип продукта, на который рассчитан прайс-лист. В зависимости от выбора заполните остальные поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Чтобы начать пользоваться прайс-листом, в поле **Состояние**, выберите **Активный**.

---

## <a name="to-set-up-a-line-discount-for-a-vendor" />Настройка скидки строки для поставщика

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Поставщики**, а затем выберите связанную ссылку.
2. Откройте соответствующую карточку поставщика и выберите действие **Скидки строки**.

   В поле **Код поставщика** заранее подставляется номер поставщика.
3. Заполните поля в строке по мере необходимости. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Заполните строку для каждой комбинации, для которой поставщик предоставляет скидку строки покупки.

## <a name="to-set-up-an-invoice-discount-for-a-vendor" />Настройка скидки по счету для поставщика

Когда поставщики проинформируют вас о том, какие скидки они предоставляют, укажите в карточках этих поставщиков коды скидок по счетам и настройте условия для каждого кода.

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Поставщики**, а затем выберите связанную ссылку.
2. Откройте карточку поставщика, который имеет право на получение скидок по счетам.
3. В поле **Код скидки по счету** выберите код соответствующих условий скидки по счету, который будет использован программой для вычисления скидок по счету для поставщика.

    > [!NOTE]  
    > Коды скидок по счету представлены существующими карточками поставщиков. Это позволяет быстро назначить условия скидки по счету поставщикам, выбрав название другого поставщика с такими же условиями.

    Перейдите к настройке новых условий скидок по счету покупки.
4. На странице **Карточка поставщика** выберите действие **Скидки по счету**. Откроется страница **Скидки по счету поставщика**.
5. В поле **Код валюты** укажите код валюты, к которой относятся условия скидки по счету в строке. Оставьте поле пустым, чтобы установить условия скидки по счету в местной валюте (руб.).
6. В поле **Минимальная сумма** введите минимальную сумму, которая должна быть на счете, чтобы для этого счета была установлена скидка.
7. В поле **Скидка (%)** введите скидку по счету в процентах от суммы счета.
8. Повторите шаги 5–7 для каждой валюты, в которой поставщик будет получать отдельную скидку по счету.

Скидка по счету теперь настроена и назначена соответствующему поставщику. При выборе кода поставщика в поле **Код скидки по счету** на других карточках поставщиков этим поставщикам назначается та же скидка по счету.

## <a name="to-choose-a-principle-for-posting-purchase-discounts" />Выбор принципа учета скидок покупки

При принятии к учету счета покупки, который включает одну или более скидок, можно выбирать между двумя принципами учета сумм скидок. Можно учитывать скидки раздельно или можно вычитать скидки из скидок счетов.  

Перед этим должны быть уже настроены необходимые счета для учета сумм скидок в плане счетов. Также следует проверить, введены ли правильные номера счетов в общих настройках учета в полях **Счет скидки строки покупки** и **Счет скидки счета покупки**.

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок введите **Настройка модуля "Покупки и кредиторская задолженность"**, а затем выберите связанную ссылку.
2. В поле **Учет скидки** выберите один из следующих принципов для учета скидок.

|**Принцип учета скидки**|**Скидка по счету**|**Скидки строки**|  
|------------------------------------|--------------------------|-----------------------|  
|**Все скидки**|Раздельный учет|Раздельный учет|  
|**Скидки счета**|Раздельный учет|Вычитается|  
|**Скидки строки**|Вычитается|Раздельный учет|  
|**Нет скидок**|Вычитается|Вычитается|  

## <a name="purchase-invoice-discounts-and-service-charges" />Скидки по счетам покупки и плата за сервисное обслуживание

Если имеются фиксированные условия предоставления скидок по счетам от конкретных поставщиков, то их можно вводить по этим поставщикам. Затем будет рассчитана скидка при заполнении счета покупки.  

Прежде чем воспользоваться скидками по счетам покупки, следует указать поставщиков, которые их предоставят.  

Можно связать процент скидки с определенными суммами счетов на страницах **Окна скидок счетов поставщиков**. Можно ввести любое число процентных ставок на каждой странице. У каждого поставщика может быть своя страница, или же можно связать несколько поставщиков с одной и той же страницей.  

Кроме процентов скидок можно связать с конкретной суммой по счету суммы платы за услуги.  

Условия скидки счета устанавливаются в локальной валюте (МВ) для отечественных поставщиков и в иностранной валюте для иностранных поставщиков.  

[!INCLUDE[prod_short](includes/prod_short.md)] позволяет производить автоматический расчет скидок по предложениям, общим заказам, заказам, счетам или кредит\-нотам.  

> [!TIP]  
> Перед вводом данной информации рекомендуется подготовить общую структуру скидок, которые предполагается использовать. Это облегчает просмотр поставщиков, ассоциированных с конкретной страницей скидок по счетам. Чем меньше страниц требуется настроить, тем быстрее можно вводить базовую информацию.

## <a name="best-price-calculation" />Расчет лучшей цены

После регистрации специальных цен и скидок по строке для покупок и продаж [!INCLUDE[prod_short](includes/prod_short.md)] гарантирует, что ваша прибыль от торговли товаром будет всегда оптимальна, автоматически рассчитывая наилучшую цену в документах продажи и покупки и в строках журнала товаров и работ.

Лучшая цена — это наиболее низкая допустимая цена с наиболее высокой допустимой скидкой строки на конкретную дату. [!INCLUDE[prod_short](includes/prod_short.md)] автоматически рассчитывает эту цену, когда вставляет цену за единицу и процент скидки по строке для товаров в строках нового документа и журнала.

> [!NOTE]  
> Ниже описано, как рассчитывается лучшая цена для продаж. Расчет выполняется аналогично для покупок.

1. [!INCLUDE[prod_short](includes/prod_short.md)] проверяются комбинацию клиента, которому выставляется счет, товара, а затем рассчитывает применимую цену за единицу и процент скидки по строке, используя следующие критерии:

    - Имеется ли для данного клиента специальное соглашение по ценами и скидкам, принадлежит ли клиент к группе, по которой указанное соглашение имеет место?
    - Включены ли товар или группа товара со скидкой для строки в какое-либо из этих соглашений по ценам и скидкам?
    - Попадает ли дата заказа (или дата учета счета и кредит-ноты) в интервал времени, начинающийся с даты начала и заканчивающийся датой окончания срока действия соглашения по ценам и скидкам?
    - Указан ли код единицы измерения? Если да, [!INCLUDE[prod_short](includes/prod_short.md)] проверяет наличие цен/скидок с одинаковыми кодами единиц измерения, а также цены/скидки, для которых коды единиц измерения не заданы.

2. [!INCLUDE[prod_short](includes/prod_short.md)] проверяет, применяются ли какие-либо соглашения по ценам и скидкам к информации в строке документа или журнала, а затем вставляет применимую цену за единицу и процент скидки по строке, используя следующие критерии:

    - Существует ли требование к минимальному количеству в соглашении по ценам и скидкам, которое выполняется?
    - Существует ли требование к валюте в соглашении по ценам и скидкам, которое выполняется? Если да, вставляется самая низкая цена и самая высокая скидка по строке для этой валюты, даже если в МВ была бы лучшая цена. Если для указанного кода валюты не имеется соглашения о ценах и скидках, [!INCLUDE[prod_short](includes/prod_short.md)] вставляет наименьшую цену и наибольшую скидку по строке, выраженную в МВ.

Если для товара в строке невозможно рассчитать специальную цену, будет вставлена либо последняя прямая себестоимость, либо цена единицы из карточки товара.

## <a name="see-related-microsoft-trainingtrainingmodulesset-up-prices-discounts-dynamics-365-business-centralindex" />См. соответствующее [обучение Microsoft](/training/modules/set-up-prices-discounts-dynamics-365-business-central/index)

## <a name="see-also" />См. также

[Настройка покупки](purchasing-setup-purchasing.md)  
[Покупки](purchasing-manage-purchasing.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
