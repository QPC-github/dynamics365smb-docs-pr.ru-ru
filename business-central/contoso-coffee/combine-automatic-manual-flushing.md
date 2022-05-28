---
title: Комбинируйте автоматическое и ручное списание
description: Пошаговое руководство для планировщика производства в Contoso Coffee, который хочет совместить автоматическое и ручное списание.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 6b128f79cb8e629147bdd5ae77f2545ad0f7025c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525185"
---
# <a name="walkthrough-combine-automatic-and-manual-flushing"></a>Пошаговое руководство: сочетание автоматического и ручного списание

В этой статье мы покажем вам, как использовать демонстрационные данные Contoso Coffee при списании.  

## <a name="scenario"></a>Сценарий

Вы являетесь планировщиком производства в Contoso Coffee. Вы должны создать новый производственный заказ на десять единиц продукта SP-SCM1004, AutoDrip. Некоторые компоненты и операции будут списываться вперед, другие списываются назад в зависимости от различных условий.

## <a name="steps"></a>Шаги

1. Создайте утвержденный производственный заказ на пять единиц продукта **SP-SCM1004, AutoDrip**. Для руководства см. [Пошаговое руководство. Создание утвержденного планового производственного заказа и его изменение](create-firm-planned-production-order-change.md).  

2. Выпустите производственный заказ.

    1. Выберите действие **Изменить статус**.  

    2. На появившейся странице установите в поле **Новый статус** как *Выпущенный*, а затем выберите кнопку **Да**.  

        Появится сообщение со строкой состояния и ссылкой на автоматическое потребление. Затем следует подтверждающее сообщение о том, что у заказа изменен статус на *Выпущенный*.  

    3. Нажмите кнопку **ОК**, чтобы закрыть сообщение с подтверждением.

3. Просмотрите операции книги товаров и производственных мощностей для производственного заказа.

    1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](../media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Запущенный производственный заказ**, а затем выберите связанную ссылку.  

    2. Откройте производственный заказ с 5 единицами кофемашины AutoDrip.  

    3. Выберите действие **Книга операций по товарам**.  

        Товар **SP-BOM1305 оцинкованный винт с шестигранной головкой M3** списывается сразу с полным ожидаемым количеством. Закройте страницу **Книга операций по товарам**.  

    4. Выберите действие **Книга операций по произв. мощностям**.  Обратите внимание, что запись операций по сборке корпуса также была завершена в момент выпуска заказа. Закройте окно **Книга операций по произв. мощностям**.

    Вы можете списать товары компонентов вручную, используя журнал потребления или производства. Ручное списание позволяет регулировать количество перед учетом. Например, если требуется дополнительное количество для покрытия низкокачественного сырья.
4. Спишите компоненты вручную.  
    1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](../media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Журнал потребления**, а затем выберите связанную ссылку.  

    2. Выберите действие **Расчет потребления**.  

    3. На странице запроса **Расчет потребления** на экспресс-вкладке **Производственный заказ** определите фильтр для определенного заказа в **Номер заказа** и нажмите кнопку **ОК**. После закрытия страницы запроса пакетного задания обратите внимание, что страница **Журнал потребления** заполняется компонентами, которые требуют ручного потребления.

    4. Выберите действие **Учет**. Закройте журнал потребления.

5. Вручную зарегистрируйте выход для электропроводки.  

    Необходимо вручную заполнить поля **Время настройки** и **Время выполнения**. Также можно указать фактически произведенное количество и брак. Введите *3* как выходное количество и учтите выход.

    1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](../media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Журнал выхода продукции**, а затем выберите связанную ссылку.  

    2. На странице **Журнал выхода продукции** создайте новую строку журнала.  

    3. В поле **Номер заказа** задайте порядок.  

    4. Выберите действие **Раскрыть маршрут**.  

        Страница **Журнал выхода продукции** заполняется строкой операции только для электропроводки.

    5. Установить поле **Время выполнения** как *10*.  

    6. Измените поле **Количество** с *5* на *3*.

    7. Выберите **Учет**.  
    8. Закройте журнал выхода продукции.

6. Просмотрите операции книги товаров для производственного заказа.

    1. На странице производственного заказа выберите действие **Книга операций по товарам**.  

    Товар **SP-BOM1302, Дисплей панели управления** учитывается с количеством *3* на основе фактического выхода, в то время как **SP-BOM1303, Кнопка** учитывается с полным ожидаемым количеством. Закройте страницу **Книга операций по товарам**.

7. Завершите производственный заказ.  

    1. Выберите действие **Изменить статус**.
    2. На появившейся странице установите в поле **Новый статус** как *Завершен*, а затем выберите кнопку **Да**.  

        Отображается сообщение со строкой состояния, отражающей автоматическое потребление. Затем следует подтверждающее сообщение о том, что заказ изменен на заказ со статусом на *Завершен*. Завершенный производственный заказ имеет тот же номер, что и в статусе *Выпущенный*.
    3. Нажмите кнопку **ОК**, чтобы закрыть сообщение с подтверждением.

8. Просмотрите операции книги товаров и производственных мощностей для производственного заказа снова.

    1. Выберите действие **Книга операций по произв. мощностям**.  

        Операция упаковочных операций завершена в момент выпуска заказа. Произведенное (выпущенное) количество — *5* независимо от результата предыдущего шага. Закройте страницу **Книга операций по произв. мощностям**.

    2. Выберите действие **Книга операций по товарам**.  

        Количество в операции книги товаров типа *Выход* равно выходному количеству в операции книги мощностей. Потребленное количество **SP-BOM1301, Корпус AutoDrip** и **SP-BOM1304, Термокувшин из нержавеющей стали** равно 5 для обоих, потому что ожидаемый результат и фактический результат совпадают. 

    3. Закройте страницу **Книга операций по товарам**.  

Вот и все для ручного и автоматического списания компонентов.

## <a name="see-also"></a>См. также

[Списание компонентов в соответствии с производственным выпуском](../production-how-to-flush-components-according-to-operation-output.md)  
[Введение в демонстрационные данные Contoso Coffee](contoso-coffee-intro.md)  