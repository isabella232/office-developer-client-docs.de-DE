---
title: PageCount-Eigenschaft (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b37ccc0c9a61e00b3c2e8f5eb3367831e5ddea43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288119"
---
# <a name="pagecount-property-ado"></a><span data-ttu-id="54bff-102">PageCount-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="54bff-102">PageCount property (ADO)</span></span>


<span data-ttu-id="54bff-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54bff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54bff-104">Gibt an, wie viele Seiten mit Daten das [Recordset](recordset-object-ado.md)-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="54bff-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="54bff-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54bff-105">Return value</span></span>

<span data-ttu-id="54bff-106">Gibt einen **Long**-Wert zurück, der die Anzahl von Seiten im **Recordset**-Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="54bff-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="54bff-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54bff-107">Remarks</span></span>

<span data-ttu-id="54bff-108">Mit der **PageCount**-Eigenschaft bestimmen Sie die Anzahl der Datenseiten im **Recordset**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="54bff-108">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="54bff-109">*Seiten* sind Datensatzgruppen, deren Größe der Einstellung der [PageSize](pagesize-property-ado.md)-Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="54bff-109">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="54bff-110">Selbst wenn die letzte Seite unvollständig ist, weil weniger Datensätze vorhanden sind, als für die **PageSize**-Eigenschaft angegeben ist, zählt sie als zusätzliche Seite für **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="54bff-110">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="54bff-111">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span><span class="sxs-lookup"><span data-stu-id="54bff-111">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="54bff-112">Weitere Informationen zur Seitenfunktionalität finden Sie unter den Eigenschaften **PageSize** und [AbsolutePage](absolutepage-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="54bff-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

