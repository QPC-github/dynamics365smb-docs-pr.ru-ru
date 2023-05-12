---
title: Управление синхронизацией основных данных
description: 'Узнайте, как управлять синхронизацией основных данных.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# Управление синхронизацией основных данных

После того как вы настроите синхронизацию основных данных и выполните синхронизацию в первый раз, записи в выбранных таблицах будут связаны и для каждой таблицы будет создана операция очереди повторяющихся заданий. Операции очереди заданий автоматически синхронизируют данные в дочерних компаниях, когда кто-либо вносит изменения в исходную компанию. Другими словами, вам больше не нужно ничего делать.

> [!NOTE]
> По умолчанию операции очереди заданий запускаются по расписанию каждую минуту, и вы не можете изменить это расписание.

Однако иногда что-то идет не так, и могут возникать ситуации, требующие вашего вмешательства или расследования. Например, если сотрудники изменят одну и ту же запись и в исходной, и в дочерней компаниях, синхронизация завершится ошибкой и вы сможете указать правильное изменение. Или исходная компания может установить расширение, которое изменит схему одной из синхронизируемых вами таблиц, добавив в нее парочку новых полей. Если вы хотите синхронизировать новые поля в дочерних компаниях, вам потребуется установить те же расширения и обновить схемы таблиц в их настройках.

В этой статье описываются инструменты, которые можно использовать для бесперебойной синхронизации.

## Расследование состояния синхронизации

На странице **Таблицы синхронизации** есть два действия, которые могут помочь вам контролировать синхронизацию:

* **Задания синхронизации интеграции**
* **Операции очереди работ**

Эти действия описаны в таблице ниже.

|Страница  |Описание  |
|---------|---------|
|**Задания синхронизации интеграции**     | Откройте страницу **Задания синхронизации интеграции**, чтобы выяснить, что происходило каждый раз при запуске операции очереди заданий. Чтобы получить более подробные сведения о новых добавленных записях или узнать, почему запись не удалось синхронизировать, выберите числа в столбцах **Вставлено** или **Ошибки**. Вы также можете использовать эту страницу для очистки старых записей, которые могут вам не понадобиться. Чтобы узнать больше об очистке, перейдите в раздел [Очистка старых операций](#clean-up-old-entries).        |
|**Операции очереди работ**     | Доступ к сведениям об операции очереди заданий, которая синхронизирует данные для выбранной таблицы. Например, вы можете использовать эту страницу для управления статусом операции очереди заданий. Чтобы узнать больше об операциях очереди заданий, перейдите к разделу [Использование очередей работ для планирования задач](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Если вы обнаружите ошибку на странице **Задания синхронизации интеграции** и не сможете устранить ее самостоятельно, то при обращении к своему партнеру или в Microsoft за поддержкой полезно предоставить сообщение об ошибке и информацию стека вызовов.

## Синхронизация измененных записей

Если вы изменяете настройку для таблицы или поля в дочерней компании, вы должны обновить синхронизацию. Например, если вы решите установить для поля флажок **Перезаписывать локальные изменения**, чтобы разрешить перезаписывать локальные изменения данными исходной компании. Для обновления синхронизации используйте действие **Синхронизировать измененные записи** на странице **Таблицы синхронизации**.

## Обновление схем таблиц

Если исходная компания изменит таблицу, например добавит в нее поле, которое вы хотите синхронизировать, дочерним компаниям потребуется обновить свои сопоставления полей. Используйте действие **Обновить поля** на странице **Поля синхронизации**. 

## Включение и отключение связей между записями

Чтобы начать или прекратить связывание определенных записей в таблице, на странице **Поля синхронизации** выберите поля, а затем используйте действие **Включить** или **Отключить**. 

> [!TIP]
> Быстрый способ включить или отключить несколько полей одновременно — выбрать их в списке, а затем использовать действие **Включить** или **Отключить**.

## Добавление расширений

Если исходная компания устанавливает новое расширение, дочерняя компания также должна установить его, если дочерней компании нужно синхронизировать данные для этого расширения. Для добавления таблиц из расширения в список дочерняя компания может использовать действие **Обновить поля** на странице **Поля синхронизации**.

> [!NOTE]
> Некоторые таблицы получают данные из связанных таблиц. Если вы добавите расширение, которое не включает связанные таблицы, поля этих таблиц будут недоступны. Убедитесь, что вы добавили все связанные таблицы.

## Очистка старых операций

Со временем количество операций в журнале синхронизации становится большим, поэтому вам может потребоваться удалить ненужные операции. Чтобы упростить очистку старых операций, на странице **Задания синхронизации интеграции** предлагаются следующие действия:

* **Удалить операции старше 7 дней**
* **Удалить все операции**

<!--
## Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## См. также

[Подготовка к синхронизации основных данных](admin-set-up-data-sync.md)