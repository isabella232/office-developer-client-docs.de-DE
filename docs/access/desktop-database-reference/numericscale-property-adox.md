---
title: NumericScale-Eigenschaft (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1a15f78463ca0ff6e690b600b9cdca7cc194c7
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025959"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="3b61c-102">NumericScale-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3b61c-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="3b61c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b61c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b61c-104">Gibt die Dezimalstelle eines numerischen Werts in der Spalte an.</span><span class="sxs-lookup"><span data-stu-id="3b61c-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3b61c-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3b61c-105">Settings and return values</span></span>

<span data-ttu-id="3b61c-p101">Legt einen Byte-Wert fest bzw. gibt einen Byte-Wert zurück, der als Skala der Datenwerte in der Spalte dient, wenn die Type-Eigenschaft auf adNumeric oder adDecimal festgelegt ist. NumericScale wird für alle anderen Datentypen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3b61c-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b61c-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b61c-108">Remarks</span></span>

<span data-ttu-id="3b61c-109">Der Standardwert lautet Null (0).</span><span class="sxs-lookup"><span data-stu-id="3b61c-109">The default value is zero (0).</span></span>

<span data-ttu-id="3b61c-110">**NumericScale** ist für [Column](column-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3b61c-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

