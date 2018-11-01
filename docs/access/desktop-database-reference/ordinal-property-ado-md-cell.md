---
title: Ordinal-Eigenschaft (ADO MD Cell)
TOCTitle: Ordinal Property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa85626b0de3a907d5a7ebf79cf333f76f42426e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867979"
---
# <a name="ordinal-property-ado-md-cell"></a><span data-ttu-id="e1e18-102">Ordinal-Eigenschaft (ADO MD Cell)</span><span class="sxs-lookup"><span data-stu-id="e1e18-102">Ordinal Property (ADO MD Cell)</span></span>


<span data-ttu-id="e1e18-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1e18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1e18-104">Identifiziert eine Zelle eindeutig durch ihre Position innerhalb einer Zellmenge.</span><span class="sxs-lookup"><span data-stu-id="e1e18-104">Uniquely identifies a cell by its position within a cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="e1e18-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e1e18-105">Return values</span></span>

<span data-ttu-id="e1e18-106">Gibt einen schreibgeschützten, ganzzahligen **Long** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e1e18-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1e18-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1e18-107">Remarks</span></span>

<span data-ttu-id="e1e18-p101">Durch den Ordnungswert einer Zelle wird die Zelle innerhalb einer Zellmenge eindeutig identifiziert. Bei diesem Konzept sind die Zellen in einer Zellmenge nummeriert, als wäre die Zellmenge ein *p*-dimensionales Array, wobei *p* die Anzahl der [Achsen](axes-collection-ado-md.md) darstellt. Zellen sind zeilenweise nummeriert (beginnend bei 0).</span><span class="sxs-lookup"><span data-stu-id="e1e18-p101">The cell's ordinal value uniquely identifies the cell within a cellset. Conceptually, cells are numbered in a cellset as if the cellset were a *p*-dimensional array, where *p* is the number of [axes](axes-collection-ado-md.md). Cells are numbered starting from zero in row-major order.</span></span>

<span data-ttu-id="e1e18-111">Der Ordnungswert der Zelle kann mit der [Item](item-property-ado-md-cellset.md)-Eigenschaft des [Cellset](cellset-object-ado-md.md)-Objekts verwendet werden, um die [Zelle](cell-object-ado-md.md) schnell abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e1e18-111">The cell's ordinal value can be used with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object to quickly retrieve the [Cell](cell-object-ado-md.md).</span></span>

