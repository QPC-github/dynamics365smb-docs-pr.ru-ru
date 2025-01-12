---
title: Организация товаров по категориям (содержит видео) | Документация Майкрософт
description: 'Чтобы находить товары, вы можете назначить им атрибуты и упорядочить их по категориям.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'category, search, attribute, facet'
ms.search.form: '5730, 5733, 5401'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="categorize-items" />Категоризация товаров

Для общего представления о товарах и упрощения их сортировки и поиска целесообразно систематизировать товары по категориям товаров.

Чтобы искать товары по характеристикам, можно назначить товарам атрибуты, а также категории товаров. Дополнительные сведения см. в разделе [Работа с атрибутами продуктов](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category" />Создание категории товара
1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок, введите **Категории товаров**, а затем выберите связанную ссылку.
2. На странице **Категории товара** выберите действие **Создать**.
3. На странице **Карточка категории товаров** заполните требуемые поля на экспресс-вкладке **Общее**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. На экспресс-вкладке **Атрибуты** укажите все атрибуты товаров для категории товара. Дополнительные сведения см. в разделе [Назначение атрибутов товаров категориям товаров](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Если категория товаров имеет родительскую категорию товаров, как указано в поле **Родительская категория**, то все атрибуты товаров, назначенные этой родительской категории, будут уже заполнены на экспресс-вкладке **Атрибуты**.

> [!NOTE]  
> Атрибуты товаров, назначенные категории товаров, автоматически применяются к товарам, которые назначены этой категории товаров.

Если вы передумали относительно категории предметов, вы можете удалить ее. Однако, если она уже была назначен элементу, вы должны удалить это назначение, прежде чем вы сможете удалить категорию элемента.

## <a name="to-assign-an-item-category-to-an-item" />Назначение товару категории товаров

1. Выберите ![Лампочка, которая открывает функцию Что вы хотите сделать.](media/ui-search/search_small.png "Что вы хотите сделать") значок введите **Товары**, а затем выберите связанную ссылку.
2. Откройте карточку товара, которому нужно присвоить категорию товаров.
3. Нажмите кнопку выбора в поле **Код товарной категории** и выберите существующую категорию товаров. Можно также выбрать действие **Создать**, чтобы сначала создать новую категорию товаров, как объясняется в разделе [Создание категории товара](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants" />Категории, атрибуты и варианты

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-related-microsoft-trainingtrainingmodulestrade-master-data-dynamics-365-business-central" />См. соответствующее [обучение Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also" />См. также

[Работа с атрибутами товаров](inventory-how-work-item-attributes.md)  
[Управление вариантами продукта](inventory-item-variants.md)  
[Регистрация новых товаров](inventory-how-register-new-items.md)  
[Запасы](inventory-manage-inventory.md)  
[Работа с [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
