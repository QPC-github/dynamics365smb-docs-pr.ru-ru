---
title: "Как преобразовывать сервисные контракты | Документы Майкрософт"
description: "Так как средство изменения ставки НДС не может преобразовать сервисные контракты, эти контракты необходимо преобразовывать вручную. В этом разделе описывается несколько альтернативных методов, которые можно использовать для преобразования сервисного контракта."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2f62bbae71eac1c0d63df5e352601c0885274066
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-convert-service-contracts-that-include-vat-amounts"></a>Практическое руководство. Преобразование сервисных контрактов, которые включают суммы НДС
Так как средство изменения ставки НДС не может преобразовать сервисные контракты, эти контракты необходимо преобразовывать вручную. В этом разделе описывается несколько альтернативных методов, которые можно использовать для преобразования сервисного контракта.  

> [!NOTE]  
>  В этом разделе дается общий обзор процесса.  

 Следующая процедура описывает, как исправить счет для контакта с предоплаченным сервисом, который был создан год назад.  

> [!NOTE]  
>  Для данного примера необходимо изменить рабочую дату на 01.01.2017.  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a>Исправление счета для предоплаченного сервисного контракта  
1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Управление контрактами**, затем выберите связанную ссылку.  
2. В разделе **Списки** выберите **Сервисные контракты**.  
3. Создайте новый предварительно оплаченный сервисный контракт. Введите начальную дату **01.01.2017** и год периода выставления счета для клиента **20000**.  
4. Этот контракт должен быть подписан. На вкладке **Главная** в группе **Процесс** выберите **Подписать контракт**.  
5. Создать сервисный счет.
6. Счет указывается как неучтенный сервисный счет. Для просмотра сервисного счета последовательно выберите **Сервис**, **Управление контрактами**, а затем — **Сервисные счета**.  
7. Выполните учет сервисного счета.  

> [!NOTE]  
>  Не изменяйте неучтенный сервисный счет. Поскольку операции книги сервиса создаются при создании счета, изменение в неучтенном счете не отразится на уже созданных операциях книги сервиса. Операции НДС создаются при учете счета. Это позволяет изменять общую товарную учетную группу и учетную товарную группу GSP в неучтенном сервисном счете.  

### <a name="to-create-a-credit-memo-for-vat-difference"></a>Создание кредит-ноты для разницы НДС  
В следующей процедуре описывается создание кредит-ноты, которая включает только разницу НДС за период, по которому уже выставлен счет, начиная с **01.07.2017**. В этом примере сумма НДС учитывается только в модуле "Финансовый менеджмент", не в модуле "Сервисное управление". Операции НДС, связанные с операцией книги сервиса, не будут исправлены.  

1. Создайте новый счет Главной книги для разницы НДС. Этот счет будет использоваться для непосредственного учета коррекции НДС.  
2. Добавьте новую строку в настройку учета НДС.  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a>Создание дат завершения контрактов по строкам контрактов  
Далее описывается процедура создания новых контрактов с использованием дат завершения контакта в строках сервисного контракта.  

1. В окне **Сервисный контракт** установите дату завершения контракта равной **30.06.2017**.  
2. Выберите действие **Создать кредит-ноту**, чтобы автоматически создать кредит-ноту с июля 2017 до декабря 2017.  
3. Поскольку срок действия контракта истек, необходимо создать новый контракт на период с новой ставкой НДС для с 1 июля 2017 по 31 декабря 2017.  

### <a name="to-create-a-new-credit-memo"></a>Создание новой кредит-ноты  
В следующей процедуре описывается создание новой кредит-ноты с помощью пакетного задания **Получить операции предоплаты по контракту**. Операции, которые не следует исправлять, с января 2017 по июнь 2017 будут удалены.  

1. Запустите средство изменения ставки НДС для 1 июля 2017 года. Общая группа учета товаров или группа учета товаров с НДС изменится. Дополнительные сведения см. в разделе [Практическое руководство. Работа с НДС по продажам и покупкам](finance-work-with-vat.md).  
2. После запуска средства изменения ставки НДС введите дату завершения сервисного контракта. Теперь можно удалять строки сервисного контракта и создавать новую строку, идентичную старой.  
3. Создайте новый счет за период с января 2017 по декабрь 2012 с использованием новой ставки НДС.  
4. Чтобы создать другую кредит-ноту, в окне **Сервисные кредит-ноты** выберите **Создать**, чтобы создать новую сервисную кредит-ноту.  
5. Выберите действие **Получение операции предопл. по контр.**.  
6. После завершения преобразование операции НДС и книги сервиса будут скорректированы.  

## <a name="see-also"></a>См. также  
[Практическое руководство. Работа с сервисными контрактами и предложениями по сервисным контрактам](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Финансы](finance.md)  
[Практическое руководство. Подача отчета об НДС в налоговые органы](finance-how-report-vat.md)  
[Практическое руководство. Работа с НДС по продажам и покупкам](finance-work-with-vat.md)  
