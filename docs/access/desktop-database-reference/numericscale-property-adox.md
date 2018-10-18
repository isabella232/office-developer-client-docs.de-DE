---
title: NumericScale-Eigenschaft (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c8cc48c2f5b2b7cc58d21890435f0d959ad1e414
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605870"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="2b2e1-102">NumericScale-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2b2e1-102">NumericScale Property (ADOX)</span></span>


<span data-ttu-id="2b2e1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b2e1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2b2e1-104">Gibt die Dezimalstelle eines numerischen Werts in der Spalte an.</span><span class="sxs-lookup"><span data-stu-id="2b2e1-104">Indicates the scale of a numeric value in the column.</span></span>

<span data-ttu-id="2b2e1-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="2b2e1-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="2b2e1-106">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2b2e1-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="2b2e1-107">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2b2e1-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="2b2e1-108">master</span><span class="sxs-lookup"><span data-stu-id="2b2e1-108">master</span></span>

<span data-ttu-id="2b2e1-p101">Legt einen Byte-Wert fest bzw. gibt einen Byte-Wert zurück, der als Skala der Datenwerte in der Spalte dient, wenn die Type-Eigenschaft auf adNumeric oder adDecimal festgelegt ist. NumericScale wird für alle anderen Datentypen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2b2e1-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b2e1-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b2e1-111">Remarks</span></span>

<span data-ttu-id="2b2e1-112">Der Standardwert lautet Null (0).</span><span class="sxs-lookup"><span data-stu-id="2b2e1-112">The default value is zero (0).</span></span>

<span data-ttu-id="2b2e1-113">**NumericScale** ist für [Column](column-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2b2e1-113">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

