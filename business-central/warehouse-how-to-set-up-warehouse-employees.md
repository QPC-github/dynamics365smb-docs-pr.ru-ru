---
title: Настройка работников склада
description: 'Каждый пользователь, который выполняет складские действия, должен быть настроен как работник склада, которому назначен один склад по умолчанию и могут быть назначены другие склады.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
---
# <a name="set-up-warehouse-employees" />Настройка работников склада

Каждый пользователь, который выполняет складские действия, должен быть настроен как работник склада, которому должен быть назначен склад по умолчанию. [!INCLUDE [prod_short](includes/prod_short.md)] отфильтровывает складские действия по складу по умолчанию, назначенному работнику. Они могут выполнять только складские действия на этом складе. Вы также можете назначить пользователя другим складам. Пользователь сможет получать доступ, но не сможет выполнять действия на этих складах.

## <a name="to-set-up-warehouse-employees" />Настройка работников склада

1. Выберите значок ![Лампочка, которая открывает функцию «Что вы хотите сделать»](media/ui-search/search_small.png "Что вы хотите сделать"), значок, введите **Работники склада**, а затем выберите связанную ссылку.  
2. Выберите действие **Создать**.  
3. Выберите поле **Код пользователя**, а затем выберите пользователя, которого необходимо добавить как работника склада. Нажмите кнопку **ОК**.  
4. В поле **Код склада** введите код склада, где будет работать пользователь.  
5. Включите переключатель **По умолчанию**, чтобы указать, что это единственный склад, где сотрудник может выполнять складские действия.  
6. Повторите эти шаги, чтобы назначить складам других работников или назначить другие склады существующим работникам склада.  

## <a name="see-related-microsoft-trainingtrainingmodulesget-started-warehouse-management" />См. соответствующее [обучение Microsoft](/training/modules/get-started-warehouse-management/)

## <a name="see-also" />См. также

[Обзор управления складом](design-details-warehouse-management.md)
[Запас](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)  
[Управление сборкой](assembly-assemble-items.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Определение политики учета счетов для пользователей](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
