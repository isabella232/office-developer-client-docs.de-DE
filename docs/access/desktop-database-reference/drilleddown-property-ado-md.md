---
title: DrilledDown-Eigenschaft (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d521176eeb2ac2e83ef05d05d3572dfba543812
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931001"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="4f5c7-102">DrilledDown-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4f5c7-102">DrilledDown property (ADO MD)</span></span>


<span data-ttu-id="4f5c7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f5c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f5c7-104">Gibt an, ob dem Element auf der Achse direkt untergeordnete Elemente folgen.</span><span class="sxs-lookup"><span data-stu-id="4f5c7-104">Indicates whether no children immediately follow the member on the axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="4f5c7-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4f5c7-105">Return values</span></span>

<span data-ttu-id="4f5c7-p101">Gibt einen schreibgeschützten **Boolean** -Wert zurück. **DrilledDown** gibt **True** zurück, wenn sich keine untergeordneten Elemente des aktuellen Elements auf der Achse befinden. **DrilledDown** gibt **False** zurück, wenn sich ein oder mehrere untergeordnete Elemente des aktuellen Elements auf der Achse befinden.</span><span class="sxs-lookup"><span data-stu-id="4f5c7-p101">Returns a **Boolean** value and is read-only. **DrilledDown** returns **True** if there are no child members of the current member on the axis. **DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f5c7-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f5c7-109">Remarks</span></span>

<span data-ttu-id="4f5c7-p102">Verwenden Sie die **DrilledDown** -Eigenschaft, um zu bestimmen, ob sich mindestens ein untergeordnetes Element in direkter Folge des aktuellen Elements auf der Achse befindet. Diese Information ist beim Anzeigen des Elements nützlich.</span><span class="sxs-lookup"><span data-stu-id="4f5c7-p102">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member. This information is useful when displaying the member.</span></span>

<span data-ttu-id="4f5c7-p103">Diese Eigenschaft wird nur für [Member](member-object-ado-md.md)-Objekte unterstützt, die zu einem [Position](position-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Level](level-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="4f5c7-p103">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

