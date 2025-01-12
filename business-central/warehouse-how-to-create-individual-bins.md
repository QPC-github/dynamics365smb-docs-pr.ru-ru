---
title: Создание ячеек
description: 'Создавайте группы одинаковых ячеек на листе создания ячеек, создавайте ячейки отдельно на карточке склада или автоматически на листе создания ячеек.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7368, 7369, 7370, 7371, 7372, 7373'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="create-bins" />Создание ячеек

Наиболее эффективным способом создания ячеек склада является генерация групп одинаковых ячеек в журнале создания ячеек, но ячейки также можно создавать по отдельности из карточки склада. Можно также использовать функцию на странице **Журнал создания ячеек** для автоматического создания ячеек.  

## <a name="to-create-a-bin-from-the-location-card" />Создание ячейки из карточки склада

1.  Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок введите **Склады**, а затем выберите связанную ссылку.  
2.  Выберите склад-источник для создания ячейки, затем выберите действие **Ячейки**.  
3. Выберите действие **Создать**.
4. Заполните соответствующим образом поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="the-dedicated-field" />Специальное поле

Поле **Специальная** на странице **Ячейки** указывает, что количества в ячейке защищены от подбора для удовлетворения других требований. Однако количества в специальных ячейках все равно могут быть зарезервированы. Соответственно, количества в специальных ячейках включаются в поле **Общее доступное кол-во** на странице **Резервирование**.

Создание выделенной ячейки создает в базовых функциях склада функциональные возможности, аналогичные использованию типов ячеек, которые доступны только в расширенных функциях склада. Дополнительные сведения см. в разделе [Настройка типов ячеек](warehouse-how-to-set-up-bin-types.md).

### <a name="example" />Пример

Производственный центр настроен с кодом ячейки в поле **Код входящей ячейки**. Строки компонента производственного заказа с этим кодом ячейки требуют, чтобы компоненты прямого списания были размещены здесь. Пока компоненты не израсходованы из этой ячейки, требования других компонентов могут выбирать из этой ячейки, так как они все еще считаются доступным содержимым ячеек. Чтобы содержимое ячейки было доступно только тому требованию на компоненты, которое использует данную ячейку, направляемую в производство, необходимо выбрать поле **Специальная** в строке этого кода ячейки.

> [!Caution]
> Товары в выделенных ячейках не защищены, когда они подбираются и потребляются как компоненты производства или сборки с помощью страницы **Подбор запасов**. Дополнительные сведения см. в разделе [Подбор для производства или сборки в базовых конфигурациях склада](warehouse-how-to-pick-for-production.md)

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet" />Создание отдельных ячеек в журнале создания ячеек

1.  Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") введите **Журнал создания ячеек**, а затем выберите связанную ссылку.  
2.  В каждой строке заполните поля, которые необходимы для названия и характеристик создаваемых ячеек.  
3.  Выберите действие **Создать ячейки**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet" />Для автоматического создания ячеек в журнале создания ячеек

Перед началом автоматического создания ячеек требуется определить вид ячеек, необходимых для работы, а также наиболее практически оправданный поток товаров по физической структуре склада.  

> [!NOTE]  
> После того как ячейка будет использована, ее можно будет удалить только в том случае, если она пуста. Но если требуется использовать другую систему именования ячеек, можно использовать журнал реклассификации, чтобы фактически переместить товары в новую систему ячеек. Однако этот процесс выполняется вручную и отнимает время, поэтому лучше всего настроить ячейки правильно с самого начала.  

Для работы со страницей **Журнал создания ячеек** вы должны иметь привилегии работника склада в местонахождении, в котором существуют ячейки. Дополнительные сведения см. в разделе [Настройка работников склада](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") введите **Журнал создания ячеек**, а затем выберите связанную ссылку.  
2.  Выберите действие **Расчет ячеек**.
3. На странице **Расчет ячеек** в поле **Код шаблона ячейки** выберите шаблон ячейки, используемый в качестве модели для создаваемых ячеек.
4.  Введите описание создаваемых ячеек.  
5.  Для создания кодов ячеек заполните поля **Начальный номер** и **Конечный номер** в трех категориях, показанных на этой странице: **Стойка**, **Секция** и **Уровень.** Код ячейки может содержать до 20 символов.  

    > [!NOTE]  
    >  Количество символов, введенных в трех категориях для каждого поля (например, символы введенные в трех полях **Начальный номер**), плюс количество разделителей полей, если они используются, не должно превышать 20.  

     В коде можно использовать буквы для идентификации, но буквы должны соответствовать тем, что используются в полях **Начальный номер** и **Конечный номер** . Например, необходимо идентифицировать часть стойки кода как **От №A01** и **До №A10**. Приложение не настроено для генерации кодов с последовательностями букв, например от A01 до F05.  

6.  Если необходимо разделить символом, таким как дефис, поля категорий, определенные как часть кода ячейки, заполните поле **Разделитель полей** данным символом.  
7.  Если необходимо, чтобы приложение не создавало строку для уже существующей ячейки, установите флажок **Проверить в существующей ячейке**.  
8. По завершении заполнения полей нажмите кнопку **ОК**.

    Приложение создает строку для каждой ячейки в журнале. Теперь можно удалить некоторые ячейки, например, если имеется ряд с проходом через два первых уровня пары секций.  

9. После удаления ненужных ячеек выберите действие **Создать ячейки**, и приложение создаст ячейки для каждой строки в журнале.  

Повторите процесс для другого набора ячеек, пока не будут созданы все ячейки на складе.  

## <a name="see-related-microsoft-trainingtrainingmodulescreate-new-bins" />См. соответствующее [обучение Microsoft](/training/modules/create-new-bins/)

## <a name="see-also" />См. также

[Обзор управления складом](design-details-warehouse-management.md)
[Запас](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)  
[Управление сборкой](assembly-assemble-items.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
