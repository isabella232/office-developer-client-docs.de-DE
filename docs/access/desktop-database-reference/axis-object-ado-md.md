---
title: Axis-Objekt (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23fdb0d9ba636ae58fa19b42d5a8a47cb01d4ab2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720730"
---
# <a name="axis-object-ado-md"></a><span data-ttu-id="eefa5-102">Axis-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="eefa5-102">Axis object (ADO MD)</span></span>


<span data-ttu-id="eefa5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eefa5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eefa5-104">Stellt eine Positions- oder Filterachse einer Zellmenge dar, die ausgewählte Elemente einer oder mehrerer Dimensionen enthält.</span><span class="sxs-lookup"><span data-stu-id="eefa5-104">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="eefa5-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eefa5-105">Remarks</span></span>

<span data-ttu-id="eefa5-106">Ein **Axis** -Objekt kann Bestandteil einer [Axes](axes-collection-ado-md.md)-Auflistung sein oder von der [FilterAxis](filteraxis-property-ado-md.md)-Eigenschaft einer [Zellmenge](cellset-object-ado-md.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eefa5-106">An **Axis** object can be contained by an [Axes](axes-collection-ado-md.md) collection, or returned by the [FilterAxis](filteraxis-property-ado-md.md) property of a [Cellset](cellset-object-ado-md.md).</span></span>

<span data-ttu-id="eefa5-107">Die Auflistungen und Eigenschaften eines **Axis** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eefa5-107">With the collections and properties of an **Axis** object, you can do the following:</span></span>

- <span data-ttu-id="eefa5-108">Identifizieren der\*\*\*\* Achse, indem Sie die [Name](name-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="eefa5-108">Identify the **Axis** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="eefa5-109">Durchlaufen der einzelnen Positionen entlang einer\*\*\*\* Achse, indem Sie die [Positions](positions-collection-ado-md.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="eefa5-109">Iterate through each position along an **Axis** using the [Positions](positions-collection-ado-md.md) collection.</span></span>

- <span data-ttu-id="eefa5-110">Abrufen der Anzahl an Dimensionen auf der\*\*\*\* Achse, indem Sie die [DimensionCount](dimensioncount-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="eefa5-110">Obtain the number of dimensions on the **Axis** with the [DimensionCount](dimensioncount-property-ado-md.md) property.</span></span>

- <span data-ttu-id="eefa5-111">Abrufen anbieterspezifischer Attribute für die\*\*\*\* Achse, indem Sie die ADO-Standardauflistung [Properties](properties-collection-ado.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="eefa5-111">Obtain provider-specific attributes of the **Axis** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

