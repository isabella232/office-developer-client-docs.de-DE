---
title: FilterAxis-Eigenschaft (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292454"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="5ac38-102">FilterAxis-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="5ac38-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="5ac38-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ac38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ac38-104">Gibt Filterinformationen zur aktuellen Zellmenge an.</span><span class="sxs-lookup"><span data-stu-id="5ac38-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="5ac38-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5ac38-105">Return values</span></span>

<span data-ttu-id="5ac38-106">Gibt ein schreibgeschütztes [Axis](axis-object-ado-md.md)-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5ac38-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac38-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ac38-107">Remarks</span></span>

<span data-ttu-id="5ac38-p101">Verwenden Sie die **FilterAxis** -Eigenschaft, um Informationen zu den Dimensionen zurückzugeben, die zum Segmentieren von Daten verwendet wurden. Die [DimensionCount](dimensioncount-property-ado-md.md)-Eigenschaft des **Axis** -Objekts gibt gibt die Anzahl der Dimensionen zurück. Diese Achse verfügt normalerweise nur über eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ac38-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="5ac38-111">Das **Axis** -Objekt, das von [FilterAxis](filteraxis-property-ado-md.md) zurückgegeben wird, ist nicht in der [Axes](axes-collection-ado-md.md)-Auflistung für ein [Cellset](cellset-object-ado-md.md)-Objekt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5ac38-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

