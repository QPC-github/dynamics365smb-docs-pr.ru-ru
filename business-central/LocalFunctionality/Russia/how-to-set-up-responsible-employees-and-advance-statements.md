---
title: Настройка материально-ответственных сотрудников и авансовых отчетов в России
description: Российские улучшения включают поддержку определения пользователей в качестве материально-ответственных сотрудников настройку авансовых отчетов, которые показывают платежи и другие документы по сотрудникам.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 5f4e3178e08b7f263d9d9a1cb86d85c5190e9aec
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738250"
---
# <a name="how-to-set-up-responsible-employees-and-advance-statements"></a>Практическое руководство. Настройка материально-ответственных сотрудников и авансовых отчетов

**Авансовый отчет** позволяет печатать и просматривать сведения о платежах, выполненных и полученных материально-ответственными лицами. Кроме того, этот отчет позволяет печатать и просматривать первичные документы по расходам материально-ответственных лиц.

## <a name="creating-the-responsible-employee-card"></a>Создание карточки подотчетного лица

Окно **Карточка подотчетного лица** создается для каждого материально-ответственного лица на основе окна **Карточка сотрудника**. Кроме того, ее можно создать отдельно.

В ней содержатся следующие сведения:

1. Номер карточки подотчетного лица.
2. Данные подотчетного лица (адрес, почтовый индекс или город, а также телефон).
3. Контактные данные (телефон, адрес электронной почты, веб-адрес).
4. Учетные финансовые данные для данного подотчетного лица на экспресс-вкладке **Учет** (**Общая бизнес группа**, **НДС бизнес группа** и **Учетная группа поставщика**).
5. Документы подотчетного лица (неучтенные и учтенные авансовые отчеты), которые можно открыть с помощью кнопки **Документы**.

Ниже показано, как открыть окно **Карточка подотчетного лица**.

### <a name="to-create-a-responsible-employee-card"></a>Создание карточки подотчетного лица

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Подотчетные лица**, затем выберите связанную ссылку.
2. Создайте новую карточку.
3. Нажмите кнопку **ОК**.

### <a name="to-create-a-responsible-employee-card-from-an-employee-card"></a>Создание карточки подотчетного лица из карточки сотрудника

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Сотрудники**, затем выберите связанную ссылку.

2. Выберите действие **Создать подотчетное лицо**.

3. Окно **Карточка подотчетного лица** содержит следующие сведения, которые вводятся вручную или из соответствующего глоссария и настроек.

   | Поле                                 | Описание                                                  |
   | ------------------------------------- | ------------------------------------------------------------ |
   | **Номер**                               | Определяет значение, которое автоматически подставляется из окна **Карточка сотрудника** или вводится вручную. |
   | **Название**                              | Определяет значение, которое автоматически подставляется из соответствующих полей окна **Карточка сотрудника** или вводится вручную. |
   | **Адрес**                           | Определяет значение, которое автоматически подставляется из соответствующих полей окна **Карточка сотрудника** или вводится вручную. |
   | **Индекс**                         | Определяет значение, которое автоматически подставляется из соответствующих полей окна **Карточка сотрудника** или вводится вручную. |
   | **Код страны/региона**               | Определяет значение, которое автоматически подставляется из соответствующих полей окна **Карточка сотрудника** или вводится вручную. |
   | **Телефон**                         | Определяет значение, которое автоматически подставляется из соответствующих полей окна **Карточка сотрудника** или вводится вручную. |
   | **Имя поиска**                       | Указывает, что значение в поле **Имя** берется из открытого окна **Карточка подотчетного лица**. |
   | **Контактные данные (адрес эл. почты, веб-адрес)** | Определяет значения, которые автоматически подставляются из соответствующих полей окна **Карточка сотрудника** или вводятся вручную. |
   | **код валюты;**                     | По умолчанию пустое значение.                                |
   | **Общая бизнес-группа**           | Определяет значение поля **Общая бизнес-группа авансового отчета** из настройки модуля "Покупки" на экспресс-вкладке **Авансовый отчет**. |
   | **НДС бизнес-группа**            | Определяет значение поля **Бизнес-группа НДС авансового отчета** из настройки модуля "Покупки" на экспресс-вкладке **Авансовый отчет**. |
   | **Учетная группа поставщика**              | Определяет значение поля **Аванс. отчет - учетная группа поставщиков** из настройки модуля "Покупки" на экспресс-вкладке **Авансовый отчет**. |

## <a name="creating-the-advance-statement"></a>Создание авансового отчета

**Авансовый отчет** создают подотчетные лица. В этом отчете содержатся сведения об оплатах, полученных сотрудниками, и о первичных документах, предоставленных для подтверждения расходов.

**Авансовый отчет** содержит следующие сведения:

- Номер авансового отчета.
- Дата учета и дата документа.
- Данные (код и имя) подотчетного лица.
- Назначение отчета и описание учета.
- Количество документов и страниц.
- Документ остатка или перерасхода для регистрации платежного документа для авансового отчета.
- Код валюты для регистрации расходов в валюте.
- Строки расходов, которые зарегистрированы в соответствии со значением, выбранным в поле **Тип в Строках Авансового Отчета** — **Счет ГК**, **Товар**, **Основные средства**, **Издержки (товар)** или **Подотчет**.

Следующие строки расходов регистрируются в соответствии со значениями, выбранными в поле **Тип** и **Номер** или **Подотчет Поставщик Но.** в строках авансового отчета:

- Чтобы списать расходы:
  - **Тип** — "Счет ГК";
  - **Номер** - Номер счета главной книги
- Чтобы отчитаться о закупленных товарах или материалах:
  - **Тип** — "Товар";
  - **Номер** - Номер карточки товара
- Чтобы отчитаться за приобретенное основное средство:
  - **Тип** — "ОС";
  - **Номер** - Номер карточки основного средства
- Чтобы отчитаться за дополнительные издержки для приобретенных товаров:
  - **Тип** — "Издержки (Товар)";
  - **Номер** - Код издержек товара.
- Чтобы зарегистрировать первичные документы, полученные от поставщика (если эти документы были получены от поставщика для товаров, основных средств или расходов подотчетного лица):
  - **Тип** — "Подотчет";
  - **Подотчет Поставщик Но.** — номер поставщика.

### <a name="to-access-the-advance-statement"></a>Чтобы открыть авансовый отчет, необходимо выполнить следующие действия.

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Авансовые отчеты**, затем выберите связанную ссылку.

   Окно **Авансовый отчет** содержит на экспресс-вкладке **Общие** в заголовке следующие сведения, введенные вручную или полученные из соответствующего глоссария или настроек.

   | Поле                                | Описание                                                  |
   | ------------------------------------ | ------------------------------------------------------------ |
   | **Номер**                              | Определяет номер авансового отчета, который рассчитывается автоматически. Номер зависит от значения поля **Серия номеров авансовых отчетов**, заданного в окне **Настройка модуля "Покупки"** на экспресс-вкладке **Авансовый отчет**. |
   | **Дата учета**, **Дата документа** | Определяет дату учета и дату документа. По умолчанию в эти поля подставляется значение рабочей даты. Его также можно заполнить вручную. |
   | **Код сотрудника**                     | Определяет номер подотчетного лица. Это значение выбирают из списка поставщиков вручную. |
   | **Имя сотрудника**                    | Определяет имя подотчетного лица. В это поле автоматически заносятся значения из полей **Имя** и **Имя2** окна **Карточка подотчетного лица**. |
   | **Назначение аванса**                  | Определяет назначение авансового платежа.                            |
   | **Описание учета**              | Задает описание учета документа. В это поле автоматически заносится значение из поля **Номер счета**. Это поле можно отредактировать вручную. |
   | **Номер счета поставщика**               | Определяет номер внешнего документа. Это поле заполняется автоматически. |
   |                                      |                                                              |

2. Окно **Авансовый отчет** содержит на экспресс-вкладке **Отчет** в заголовке следующие сведения, введенные вручную или полученные из соответствующего глоссария или настроек.

   | Поле                                  | Описание                                                  |
   | -------------------------------------- | ------------------------------------------------------------ |
   | **Кол-во документов**, **Кол-во страниц** | Определяет количество документов, подтверждающих расходы, и количество страниц в этих документах. Эти поля заполняют вручную, вписывая числовые значения. |
   | **Номер документа остатка/перерасхода**    | Определяет денежный документ, закрывающий сумму остатка или перерасхода для данного авансового отчета. Платежный документ выбирают из операций Книги поставщиков для данного подотчетного лица. |

   Окно **Авансовый отчет** содержит следующие сведения из созданных строк расходов.

   | Поле                                                        | Описание                                                  |
   | ------------------------------------------------------------ | ------------------------------------------------------------ |
   | **Тип**                                                     | Выберите тип "Счет ГК", "Товар", "ОС", "Издержки (Товар)" или "Подотчет", в зависимости от типа расходов. |
   | **Номер**                                                      | Если в поле "Тип" содержится **Счет ГК**: в поле **Номер** выберите счет ГК из глоссария "Список финансовых счетов".   Если "Тип" = **Товар**: в поле **Номер** выберите карточку товара из глоссария "Список товаров".   Если в поле "Тип" содержится **ОС**: в поле **Номер** выберите карточку основного средства из глоссария "Список основных средств".   Если "Тип" = **Издержки (товар)**: в поле **Номер** выберите издержки товара из глоссария "Издержки товаров и основных средств". |
   | **Подотчет - номер поставщика**                                | Если "Тип" = **Подотчет**: в поле **Подотчет - номер поставщика** выберите карточку поставщика из глоссария "Список поставщиков". |
   | **Подотчет - номер операции**                                  | Если "Тип" = **Подотчет**: В поле **Подотчет - номер операции** выберите учтенную операцию поставщика из финансовых операций поставщика. **Примечание**. В случае если подотчетного лицо получает от поставщика первичные документы (например, счет-фактуру), до регистрации авансового отчета необходимо учесть счет от поставщика. |
   | **Подотчет - номер документа**, **Подотчет - дата документа** | Эти поля заполняют вручную. В поле **Подотчет - номер документа** нужно ввести номер документа, подтверждающего расходы в текущей строке.   В поле **Подотчет - дата документа** укажите дату документа, подтверждающего расходы в текущей строке. |
   | **Описание**                                              | Описание расходов в текущей строке. По умолчанию в поле **Описание** вносится значение поля **Имя** или **Описание** из выбранной карточки. |
   | **Количество** **Прямые затраты без НДС**                      | Количество и сумма расходов (товары и основные средства). Эти поля заполняют вручную, вписывая числовые значения. |

   В поле **Статус Созданного Документа** приводится статус текущего документа. Чтобы изменить этот статус с **Открыт** на **Выпущен**, необходимо выполнить следующие действия.

3. Выберите действие **Выпустить**. Выпущенный авансовый отчет можно будет напечатать.

## <a name="printing-an-unposted-advance-statement"></a>Печать неучтенного авансового отчета

Ниже показано, как напечатать неучтенный авансовый отчет.

### <a name="to-print-an-unposted-advance-statement"></a>Печать неучтенного авансового отчета

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Авансовые отчеты**, затем выберите связанную ссылку.

2. В окне **Авансовый отчет** выберите действие **Печать**.

    Примечание

   Отчет обычно печатают после создания документа для подписи и подтверждения.

3. На экспресс-вкладке **Заголовок покупки** примените следующие фильтры.

   | Поле             | Фильтр                                                       |
   | ----------------- | ------------------------------------------------------------ |
   | **Номер**           | В этом поле указан номер неучтенного авансового отчета. По умолчанию берется значение из открытого документа. |
   | **Тип документа** | Это поле заполняется автоматически.                       |

4. На экспресс-вкладке **Параметры** укажите сотрудников, обязанных подписать данный документ, как показано в таблице ниже.

   | Параметр              | Описание                                                  |
   | ---------------------- | ------------------------------------------------------------ |
   | Бухгалтер (Кассир) | Выберите код сотрудника (кассира) из таблицы "Список сотрудников", чтобы заполнить соответствующие поля отчета. |
   | Бухгалтер             | Выберите код сотрудника (бухгалтера) из таблицы "Список сотрудников", чтобы заполнить соответствующие поля отчета. |

5. Нажмите кнопку **Печать**.

## <a name="viewing-the-posted-advance-statement"></a>Просмотр учтенного авансового отчета

В следующей процедуре показано, как открыть учтенный **Авансовый отчет**.

### <a name="to-view-the-posted-advance-statement"></a>Просмотр учтенного авансового отчета

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Учтенный авансовый отчет**, затем выберите связанную ссылку.

В учтенном авансовом отчете указаны все сведения, введенные в документ в форме **Авансовый отчет**.

## <a name="printing-the-posted-advance-statement"></a>Печать учтенного авансового отчета

Ниже показано, как напечатать учтенный **Авансовый отчет**.

### <a name="to-print-a-posted-advance-statement"></a>Печать учтенного авансового отчета

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Учтенные авансовые отчеты**, затем выберите связанную ссылку.

2. Выберите действие **Печать**. Откроется диалоговое окно **Учтенный авансовый отчет**.

    Примечание

   Такой отчет обычно печатают как утвержденный и подтвержденный документ.

3. На экспресс-вкладке **Заголовок счета покупки** отчета примените следующие фильтры.

   | Поле   | Фильтр                                                       |
   | ------- | ------------------------------------------------------------ |
   | **Номер** | По умолчанию в этом поле указан номер учтенного авансового отчета. По умолчанию это значение берется из открытого документа. |

4. На экспресс-вкладке **Параметры** укажите сотрудников для подписи данного документа, как показано в таблице ниже.

   | Параметр            | Описание                                                  |
   | -------------------- | ------------------------------------------------------------ |
   | Бухгалтер (Кассир) | Выберите код сотрудника (кассира) из таблицы "Список сотрудников", чтобы заполнить соответствующие поля отчета. |
   | Бухгалтер           | Выберите код сотрудника (бухгалтера) из таблицы "Список сотрудников", чтобы заполнить соответствующие поля отчета. |

5. Нажмите кнопку **Печать**.

## <a name="see-also"></a>См. также

[Персонал](../../hr-manage-human-resources.md)  