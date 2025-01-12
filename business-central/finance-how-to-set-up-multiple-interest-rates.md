---
title: Настройка нескольких процентных ставок для отложенного платежа
description: 'В этой теме объясняется, как вычислять финансовые сборы с несколькими процентными ставками за определенный период.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '6, 431, 432, 572'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="set-up-multiple-interest-rates-for-delayed-payment" />Настройка нескольких процентных ставок для отложенного платежа

Можно использовать разные процентные ставки для различных периодов для задержанных платежей в торговых транзакциях. [!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)]

Например, государство определяет максимальный процент, начисляемый потребителю. Данную процентную ставку можно изменять дважды в год 1-го января и 1-го июля. Процентная ставка между компаниями (B2B) устанавливается по соглашению сторон, и для этой группе клиентов нет ограничений. Объявленная ставка обычно на 4 процента выше обычного банковского процента.

При создании условий финансовых ставок и условий напоминания для штрафов за задержанный платеж можно определить несколько процентных ставок, чтобы начисленные пени вычислялись с разными процентными ставками за различные периоды.  

## <a name="to-set-up-multiple-interest-rates" />Настройка нескольких процентных ставок

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Процентные ставки**, а затем выберите связанную ссылку.  
2. На странице **Процентные ставки** выберите требуемые финансовые условия, затем выберите действие **Процентные ставки**.  
3. Заполните соответствующим образом поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Нажмите кнопку **ОК**.  
5. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Уровни напоминания**, а затем выберите связанную ссылку.  
6. На странице **Условия напоминания** выберите требуемые условия напоминания, затем выберите действие **Уровни**.  
7. На странице **Уровни напоминаний** для соответствующих уровней напоминания выберите поле **Рассчитать проценты**.  

При выпуске процент-ноты в ней отображаются финансовые сборы с несколькими процентными ставками за определенный период времени. Кредит-нота также содержит контактные сведения клиента, организации, выпускающей кредит-ноту, дополнительную сумму и общую сумму. Открывающая операция кредит-ноты отображается жирным шрифтом. Финансовые сборы рассчитываются с несколькими процентными ставками для определенного временного периода и печатаются после открывающей операции кредит-ноты.  

## <a name="see-also" />См. также

[Сбор непогашенных остатков задолженности](receivables-collect-outstanding-balances.md)  
[Настройка финансов](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
