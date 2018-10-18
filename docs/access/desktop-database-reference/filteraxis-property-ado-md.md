---
title: FilterAxis-Eigenschaft (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32ddf737ae0d6aa9a7b2daf8adc2a07707c91c0c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603056"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="324d1-102">FilterAxis-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="324d1-102">FilterAxis Property (ADO MD)</span></span>


<span data-ttu-id="324d1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="324d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="324d1-104">Gibt Filterinformationen zur aktuellen Zellmenge an.</span><span class="sxs-lookup"><span data-stu-id="324d1-104">Indicates filter information about the current cellset.</span></span>

<span data-ttu-id="324d1-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="324d1-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="324d1-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="324d1-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="324d1-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="324d1-107">Return values</span></span>
>>>>>>> <span data-ttu-id="324d1-108">master</span><span class="sxs-lookup"><span data-stu-id="324d1-108">master</span></span>

<span data-ttu-id="324d1-109">Gibt ein schreibgeschütztes [Axis](axis-object-ado-md.md)-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="324d1-109">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="324d1-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="324d1-110">Remarks</span></span>

<span data-ttu-id="324d1-p101">Verwenden Sie die **FilterAxis** -Eigenschaft, um Informationen zu den Dimensionen zurückzugeben, die zum Segmentieren von Daten verwendet wurden. Die [DimensionCount](dimensioncount-property-ado-md.md)-Eigenschaft des **Axis** -Objekts gibt gibt die Anzahl der Dimensionen zurück. Diese Achse verfügt normalerweise nur über eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="324d1-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="324d1-114">Das **Axis** -Objekt, das von [FilterAxis](filteraxis-property-ado-md.md) zurückgegeben wird, ist nicht in der [Axes](axes-collection-ado-md.md)-Auflistung für ein [Cellset](cellset-object-ado-md.md)-Objekt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="324d1-114">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

