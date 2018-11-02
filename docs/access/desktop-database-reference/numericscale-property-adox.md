---
title: NumericScale-Eigenschaft (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7dd53830216c302d68adf44e1bea88bbc52e980
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921313"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="c7cd1-102">NumericScale-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c7cd1-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="c7cd1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7cd1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7cd1-104">Gibt die Dezimalstelle eines numerischen Werts in der Spalte an.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c7cd1-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c7cd1-105">Settings and return values</span></span>

<span data-ttu-id="c7cd1-p101">Legt einen Byte-Wert fest bzw. gibt einen Byte-Wert zurück, der als Skala der Datenwerte in der Spalte dient, wenn die Type-Eigenschaft auf adNumeric oder adDecimal festgelegt ist. NumericScale wird für alle anderen Datentypen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7cd1-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7cd1-108">Remarks</span></span>

<span data-ttu-id="c7cd1-109">Der Standardwert lautet Null (0).</span><span class="sxs-lookup"><span data-stu-id="c7cd1-109">The default value is zero (0).</span></span>

<span data-ttu-id="c7cd1-110">**NumericScale** ist für [Column](column-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

