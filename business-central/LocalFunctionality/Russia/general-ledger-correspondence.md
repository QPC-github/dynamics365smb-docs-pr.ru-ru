---
title: Корреспонденция финансовых операций в России
description: Российские улучшения включают корреспонденцию финансовых операций.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: c3a065046eaa12a76c98bdd7c8ce9fd0a3374ff5
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738221"
---
# <a name="general-ledger-correspondence"></a>Корреспонденция финансовых операций

Функция корреспонденции финансовых операций позволяет: 

- Периодически создавать транзакцию корреспонденции.
- Учитывать операции корреспонденции при учете финансовых транзакций.
- Анализировать ряд отчетов для корреспонденции.

 

## <a name="creating-a-general-ledger-correspondence-entry"></a>Создание операции финансовой корреспонденции

 

Ниже приводится процедура периодического создания операций финансовой корреспонденции.

 

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Создать корреспонденцию счетов**, затем выберите связанную ссылку.
2. Введите в поле **Номер транзакции** номер транзакции, если финансовая корреспонденция должна быть создана только для выбранной транзакции. В противном случае оставьте поле пустым.

 

Чтобы настроить автоматическую финансовую корреспонденцию

 

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка ГК**, затем выберите связанную ссылку.
2. Установите флажок **Авт. корреспонденция**.

 

## <a name="reports"></a>Отчеты

 

Следующие отчеты были добавлены для анализа данных из транзакций корреспонденции:

 

- Фин. Корресп. Главная Книга (страница 12403; отчет 12431)
- Операции корреспонденции (страница 12401)
- Отчет Фин. Корресп. Журнал-Ордер (отчет 12432)
- Отчет Фин. Корресп. Анализ Операций (отчет 12435)

 

### <a name="general-ledger---correspondence-window"></a>Окно "Фин. Корресп. Главная Книга"

 

Окно **Фин. Корресп. Главная Книга** отображает обороты по корреспонденции счетов за выбранный период.

 

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Корреспонденция**, затем выберите связанную ссылку.
2. Выберите действие **Фин. Корресп. Главная Книга**.

 

Заголовок окна **Фин. Корресп. Главная Книга** содержит следующие фильтры:

 

- Фильтр по дате
- Фильтр по филиалу
- Фильтр по глобальному измерению 1
- Фильтр по глобальному измерению 2

 

В подформе отчета показан оборот в корреспонденции с другими счетами:

![Фин. Корресп. Главная Книга](General-Ledger-Correspondence.png)

 

### <a name="gl-corresp-entries-analysis-report"></a>Отчет Фин. Корресп. Анализ Операций

 

**Отчет Фин. Корресп. Анализ Операций** отображает записи корреспонденции для каждого счета. Отчет может использоваться для обзора операций по счету главной книги с корреспондированием и итоговыми суммами.

 

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Корреспонденция**, затем выберите связанную ссылку.
2. Выберите действие **Фин. Корресп. Анализ Операций**.

 

На вкладке **Параметры** формы запроса имеется возможность задать параметры, заполнив поля сведениями, описанными в следующей таблице.

 

| Поле                                                        | Описание                                                  |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| **Начало периода**                                         | Введите дату начала периода для операций, которые нужно включить в отчет. |
| **Окончание периода**                                         | Введите дату окончания периода для операций, которые нужно включить в отчет. |
| **Другие параметры**:<br />**Без нулевых оборотов**, **Без нулевых строк**, **Дебет и кредит раздельно**, **Новая страница для счета ГК** | Указание представления отчета, например, нужно ли выводить сведения для каждого счета без нулевых строк или нулевых оборотов. |

 

## <a name="see-also"></a>См. также

 

[Функциональность локальной версии для России](russia-local-functionality.md)
