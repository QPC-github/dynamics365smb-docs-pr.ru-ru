---
title: "Настройка новых организаций с помощью командлета | Документы Майкрософт"
description: "В некоторых сценариях может потребоваться загрузить и импортировать пакет конфигурации без участия пользователей или без использования пользовательского интерфейса служб RapidStart Services. Для этого можно воспользоваться командлетом Windows PowerShell."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Настройка новых организаций с помощью командлета
В некоторых сценариях может потребоваться загрузить и импортировать пакет конфигурации без участия пользователей или без использования пользовательского интерфейса служб RapidStart Services. Для этого можно воспользоваться командлетом Windows PowerShell. Ниже перечислены сценарии, в которых это может быть полезно.  

- Выполнение импорта данных сразу для нескольких установок [!INCLUDE[d365fin](includes/d365fin_md.md)].
- Настройка дополнительных областей приложения для нескольких клиентов.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Развертывание пакета конфигурации с использованием командлета  

1. Подготовьте пакет служб RapidStart Services. Например, можно создать пакет для импорта определенных значений, а также имена таблиц и полей, в которые следует вставить эти значения.  
2. Установите пакет на компьютере, на котором будет выполняться командлет.  
3. Откройте оболочку администрирования [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4. Введите **Invoke-NAVCodeUnit** и укажите сведения, как описано в следующем примере.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
Командлет импортирует пакет в каждую компанию. Пользователи могут немедленно приступить к использованию новой функции.  

## <a name="see-also"></a>См. также  
[Настройка новых организаций](admin-how-to-configure-new-companies.md)  
[Применение конфигураций к новым организациям](admin-apply-configuration-to-new-companies.md)  
[Настройка компании с помощью служб RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Администрация](admin-setup-and-administration.md)  
[Командлеты Windows PowerShell для Microsoft Dynamics NAV](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)
