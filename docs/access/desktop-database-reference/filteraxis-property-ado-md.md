---
title: FilterAxis-Eigenschaft (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 214de72e71a51c6b6b65bc2636a28e5650035c0a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926906"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="3bce0-102">FilterAxis-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3bce0-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="3bce0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bce0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bce0-104">Gibt Filterinformationen zur aktuellen Zellmenge an.</span><span class="sxs-lookup"><span data-stu-id="3bce0-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="3bce0-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3bce0-105">Return values</span></span>

<span data-ttu-id="3bce0-106">Gibt ein schreibgeschütztes [Axis](axis-object-ado-md.md)-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3bce0-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bce0-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3bce0-107">Remarks</span></span>

<span data-ttu-id="3bce0-p101">Verwenden Sie die **FilterAxis** -Eigenschaft, um Informationen zu den Dimensionen zurückzugeben, die zum Segmentieren von Daten verwendet wurden. Die [DimensionCount](dimensioncount-property-ado-md.md)-Eigenschaft des **Axis** -Objekts gibt gibt die Anzahl der Dimensionen zurück. Diese Achse verfügt normalerweise nur über eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="3bce0-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="3bce0-111">Das **Axis** -Objekt, das von [FilterAxis](filteraxis-property-ado-md.md) zurückgegeben wird, ist nicht in der [Axes](axes-collection-ado-md.md)-Auflistung für ein [Cellset](cellset-object-ado-md.md)-Objekt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3bce0-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

