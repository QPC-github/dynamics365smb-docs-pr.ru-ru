---
title: Настройка предоплат клиентов в России
description: Российские улучшения включают предоплату клиентов.
author: DianaMalina
ms.topic: conceptual
ms.search.keywords: null
ms.date: 04/01/2021
ms.reviewer: edupont
ms.author: soalex
---

# <a name="set-up-customer-prepayments" />Настройка предоплат клиентов

Предоплаты — это авансовые платежи по заказам на продажу, которые получены, для которых создан счет и которые учтены, но до окончательного выставления счетов. Например, вам может потребоваться задаток, чтобы произвести товар и отгрузить его клиенту. Предоплаты позволяют создавать счета и собирать авансовые платежи от клиентов и учитывать платежи для правильных счетов.

## <a name="to-set-up-customer-prepayments" />Настройка предоплат клиентов

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](../../media/ui-search/search_small.png "Что вы хотите сделать") значок введите **Настройка модуля "Продажи и дебиторская задолженность"**, а затем выберите связанную ссылку.

2. На экспресс-вкладке **Нумерация** убедитесь, что серия номеров **Серия номеров учт. счетов предопл.** совпадает с **Серия номеров учт. счетов**. Убедитесь также, что серия номеров для **Серия номеров учт. кр.-нот предопл.** совпадает с серией для **Серия номеров учт. кредит-нот**.

3. На экспресс-вкладке **Предоплата** введите следующие сведения.

   | Поле                             | Описание                                                  |
   | :-------------------------------- | :----------------------------------------------------------- |
   | **Использовать счет ГК предоплаты**        | Выберите это поле, чтобы учесть предоплаты поставщикам, используя субсчет, указанный в поле **Счет предоплаты** в окне **Учетные группы клиента**. |
   | **Создание счета на предоплату**     | Выберите, чтобы создать счет на предоплату. Если это поле не выбрано, счет на предоплату создан не будет. |
   | **Серия номеров учт. предоплат**        | Введите код серии номеров, который требуется использовать для счетов на предоплату. |
   | **Учт. разн. по предопл. - серия ном. док.**           | Введите код серии номеров, который требуется использовать для документов предоплаты. |
   | **Разн. по предопл. - тип серии номеров док.**             | Укажите, требуется ли использовать серию номеров или символ для идентификации документов предоплаты. |
   | **Символ для док. разн. по предопл.**            | Введите символ, который будет печататься на документах предоплаты.        |
   | **Разн. по предопл.: прибыль - знач. изм. условия**  | Введите код для измерения, которое используется для создания условной прибыли от предоплаты. |
   | **Разн. по предопл.: убытки - знач. изм. условия** | Введите код для измерения, которое используется для создания условного убытка от предоплаты. |
   | **Разн. по предопл.: прибыль - знач. изм. вида**       | Введите код для измерения, которое используется для создания платежа с точки зрения прибыли от предоплаты. |
   | **Разн. по предопл.: убытки - знач. изм. вида**      | Введите код для измерения, которое используется для создания платежа с точки зрения прибыли от предоплаты. |

4. Откройте окно **Учетные группы клиента**.

5. В поле **Счет предоплаты** укажите счет главной книги, который должен использоваться для учета предоплаты клиентов.

6. Нажмите кнопку **Закрыть**, чтобы закрыть окно и сохранить введенные данные.

Теперь вы можете создавать счета и собирать авансовые платежи от клиентов и учитывать платежи для правильных счетов.

## <a name="see-also" />См. также

[Выставление счетов на предоплату](../../finance-invoice-prepayments.md)  
[Пошаговое руководство. Настройка и выставление счетов на продажу](../../walkthrough-setting-up-and-invoicing-sales-prepayments.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
