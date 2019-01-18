---
title: Precision-Eigenschaft (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f05f6880a9599421189519f263cfb27bf1432325
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726162"
---
# <a name="precision-property-adox"></a><span data-ttu-id="cad1b-102">Precision-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cad1b-102">Precision property (ADOX)</span></span>


<span data-ttu-id="cad1b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cad1b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cad1b-104">Gibt die maximale Genauigkeit von Datenwerten in der Spalte an.</span><span class="sxs-lookup"><span data-stu-id="cad1b-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cad1b-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="cad1b-105">Settings and return values</span></span>

<span data-ttu-id="cad1b-p101">Legt einen **Long** -Wert fest bzw. gibt diesen zurück. Der Wert ist die maximale Genauigkeit von Datenwerten in der Spalte, wenn die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)-Eigenschaft ein numerischer Typ ist. **Precision** wird für alle anderen Datentypen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cad1b-p101">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is a numeric type. **Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="cad1b-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cad1b-108">Remarks</span></span>

<span data-ttu-id="cad1b-109">Der Standardwert lautet Null (0).</span><span class="sxs-lookup"><span data-stu-id="cad1b-109">The default value is zero (0).</span></span>

<span data-ttu-id="cad1b-110">Diese Eigenschaft ist schreibgeschützt für [Column](column-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="cad1b-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

