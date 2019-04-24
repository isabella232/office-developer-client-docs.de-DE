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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296899"
---
# <a name="axis-object-ado-md"></a><span data-ttu-id="36d49-102">Axis-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="36d49-102">Axis object (ADO MD)</span></span>


<span data-ttu-id="36d49-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="36d49-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36d49-104">Stellt eine Positions- oder Filterachse einer Zellmenge dar, die ausgewählte Elemente einer oder mehrerer Dimensionen enthält.</span><span class="sxs-lookup"><span data-stu-id="36d49-104">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="36d49-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36d49-105">Remarks</span></span>

<span data-ttu-id="36d49-106">Ein **Axis**-Objekt kann Bestandteil einer [Axes](axes-collection-ado-md.md)-Auflistung sein oder von der [FilterAxis](filteraxis-property-ado-md.md)-Eigenschaft einer [Zellmenge](cellset-object-ado-md.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="36d49-106">An **Axis** object can be contained by an [Axes](axes-collection-ado-md.md) collection, or returned by the [FilterAxis](filteraxis-property-ado-md.md) property of a [Cellset](cellset-object-ado-md.md).</span></span>

<span data-ttu-id="36d49-107">Die Auflistungen und Eigenschaften eines **Axis**-Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="36d49-107">With the collections and properties of an **Axis** object, you can do the following:</span></span>

- <span data-ttu-id="36d49-108">Identifizieren der\*\*\*\* Achse, indem Sie die [Name](name-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="36d49-108">Identify the **Axis** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="36d49-109">Durchlaufen der einzelnen Positionen entlang einer\*\*\*\* Achse, indem Sie die [Positions](positions-collection-ado-md.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="36d49-109">Iterate through each position along an **Axis** using the [Positions](positions-collection-ado-md.md) collection.</span></span>

- <span data-ttu-id="36d49-110">Abrufen der Anzahl an Dimensionen auf der\*\*\*\* Achse, indem Sie die [DimensionCount](dimensioncount-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="36d49-110">Obtain the number of dimensions on the **Axis** with the [DimensionCount](dimensioncount-property-ado-md.md) property.</span></span>

- <span data-ttu-id="36d49-111">Abrufen anbieterspezifischer Attribute für die\*\*\*\* Achse, indem Sie die ADO-Standardauflistung [Properties](properties-collection-ado.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="36d49-111">Obtain provider-specific attributes of the **Axis** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

