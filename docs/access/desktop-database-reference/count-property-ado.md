---
title: Count-Eigenschaft (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a341a82e5cdc9ed5a55ca9f4b80ba80c6875bf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713534"
---
# <a name="count-property-ado"></a><span data-ttu-id="887aa-102">Count-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="887aa-102">Count property (ADO)</span></span>


<span data-ttu-id="887aa-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="887aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="887aa-104">Gibt die Anzahl von Objekten in einer Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="887aa-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="887aa-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="887aa-105">Return value</span></span>

<span data-ttu-id="887aa-106">Gibt einen Wert vom Datentyp **Long** zurück.</span><span class="sxs-lookup"><span data-stu-id="887aa-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="887aa-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="887aa-107">Remarks</span></span>

<span data-ttu-id="887aa-108">Mit der **Count** -Eigenschaft bestimmen Sie, wie viele Objekte in einer bestimmten Auflistung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="887aa-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="887aa-p101">Die Nummerierung für Auflistungselemente beginnt bei Null, weshalb Sie im Code Schleifen stets mit dem Element Null beginnen und mit dem Wert der **Count** -Eigenschaft minus 1 beenden sollten. Falls Sie Microsoft Visual Basic verwenden und Schleifen durch die Auflistungselemente ausführen möchten, ohne die **Count** -Eigenschaft zu überprüfen, verwenden Sie den Befehl **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="887aa-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="887aa-111">Wenn die **Count** -Eigenschaft gleich null ist, sind in der Auflistung keine Objekte vorhanden.</span><span class="sxs-lookup"><span data-stu-id="887aa-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

