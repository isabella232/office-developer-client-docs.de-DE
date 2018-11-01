---
title: PageCount-Eigenschaft (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef5179f44a2c7c153411ae33566f3806f1e93573
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867370"
---
# <a name="pagecount-property-ado"></a><span data-ttu-id="c0f41-102">PageCount-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="c0f41-102">PageCount property (ADO)</span></span>


<span data-ttu-id="c0f41-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0f41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0f41-104">Gibt an, wie viele Seiten mit Daten das [Recordset](recordset-object-ado.md)-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="c0f41-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0f41-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0f41-105">Return value</span></span>

<span data-ttu-id="c0f41-106">Gibt einen **Long** -Wert zurück, der die Anzahl von Seiten im **Recordset** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="c0f41-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0f41-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0f41-107">Remarks</span></span>

<span data-ttu-id="c0f41-p101">Bestimmen Sie mit der PageCount-Eigenschaft, wie viele Seiten mit Daten in einem Recordset-Objekt enthalten sind. Seiten sind Datensatzgruppen, deren Größe der Einstellung der PageSize-Eigenschaft entspricht. Die letzte Seite wird auch dann als weitere Seite im PageCount-Wert gezählt, wenn sie nicht vollständig ist, weil sie weniger Datensätze enthält als der PageSize-Wert angibt. Wird diese Eigenschaft vom Recordset-Objekt nicht unterstützt, gibt der Wert -1 an, dass PageCount nicht bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0f41-p101">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object. *Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting. Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="c0f41-112">Weitere Informationen zur Seitenfunktionalität finden Sie unter den Eigenschaften **PageSize** und [AbsolutePage](absolutepage-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c0f41-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

