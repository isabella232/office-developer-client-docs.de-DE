---
title: Precision-Eigenschaft (ADOX)
TOCTitle: Precision Property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5fab2a7dc7a2d9f05e22b064acfaeabf93106a3e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473064"
---
# <a name="precision-property-adox"></a><span data-ttu-id="678b1-102">Precision-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="678b1-102">Precision Property (ADOX)</span></span>


<span data-ttu-id="678b1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="678b1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="678b1-104">Gibt die maximale Genauigkeit von Datenwerten in der Spalte an.</span><span class="sxs-lookup"><span data-stu-id="678b1-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="678b1-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="678b1-105">Settings and Return Values</span></span>

<span data-ttu-id="678b1-p101">Legt einen **Long** -Wert fest bzw. gibt diesen zurück. Der Wert ist die maximale Genauigkeit von Datenwerten in der Spalte, wenn die [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\))-Eigenschaft ein numerischer Typ ist. **Precision** wird für alle anderen Datentypen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="678b1-p101">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is a numeric type. **Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="678b1-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="678b1-108">Remarks</span></span>

<span data-ttu-id="678b1-109">Der Standardwert lautet Null (0).</span><span class="sxs-lookup"><span data-stu-id="678b1-109">The default value is zero (0).</span></span>

<span data-ttu-id="678b1-110">Diese Eigenschaft ist schreibgeschützt für [Column](column-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="678b1-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

