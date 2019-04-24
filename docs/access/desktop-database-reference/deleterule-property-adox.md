---
title: DeleteRule-Eigenschaft (ADOX)
TOCTitle: DeleteRule property (ADOX)
ms:assetid: cd05e024-c1fc-a0b8-8ada-e05ec899c334
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250018(v=office.15)
ms:contentKeyID: 48547752
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb7d1e5f6a25fc92d43d9e75181a3651a2031856
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294008"
---
# <a name="deleterule-property-adox"></a><span data-ttu-id="0b0ec-102">DeleteRule-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="0b0ec-102">DeleteRule property (ADOX)</span></span>


<span data-ttu-id="0b0ec-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b0ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b0ec-104">Gibt die ausgeführte Aktion an, wenn ein Primärschlüssel gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="0b0ec-104">Indicates the action performed when a primary key is deleted.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0b0ec-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0b0ec-105">Settings and return values</span></span>

<span data-ttu-id="0b0ec-p101">Legt einen **Long**-Wert fest und gibt diesen zurück. Der Wert kann eine der [RuleEnum](ruleenum.md)-Konstanten sein kann. Der Standardwert lautet **adRINone**.</span><span class="sxs-lookup"><span data-stu-id="0b0ec-p101">Sets and returns a **Long** value that can be one of the [RuleEnum](ruleenum.md) constants. The default value is **adRINone**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b0ec-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b0ec-108">Remarks</span></span>

<span data-ttu-id="0b0ec-109">Diese Eigenschaft ist schreibgeschützt für [Key](key-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="0b0ec-109">This property is read-only on [Key](key-object-adox.md) objects already appended to a collection.</span></span>

