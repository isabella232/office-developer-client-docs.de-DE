---
title: NumericScale-Eigenschaft (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709054"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="91f92-102">NumericScale-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="91f92-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="91f92-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91f92-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91f92-104">Gibt die Dezimalstelle eines numerischen Werts in der Spalte an.</span><span class="sxs-lookup"><span data-stu-id="91f92-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="91f92-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="91f92-105">Settings and return values</span></span>

<span data-ttu-id="91f92-p101">Legt einen Byte-Wert fest bzw. gibt einen Byte-Wert zurück, der als Skala der Datenwerte in der Spalte dient, wenn die Type-Eigenschaft auf adNumeric oder adDecimal festgelegt ist. NumericScale wird für alle anderen Datentypen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="91f92-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="91f92-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91f92-108">Remarks</span></span>

<span data-ttu-id="91f92-109">Der Standardwert lautet Null (0).</span><span class="sxs-lookup"><span data-stu-id="91f92-109">The default value is zero (0).</span></span>

<span data-ttu-id="91f92-110">**NumericScale** ist für [Column](column-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="91f92-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

