---
title: CellSet-Objekt (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296514"
---
# <a name="cellset-object-ado-md"></a><span data-ttu-id="e3f0a-102">CellSet-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e3f0a-102">Cellset object (ADO MD)</span></span>

<span data-ttu-id="e3f0a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3f0a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3f0a-104">Stellt die Ergebnisse einer multidimensionalen Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-104">Represents the results of a multidimensional query.</span></span> <span data-ttu-id="e3f0a-105">Es ist eine Auflistung von Zellen, die aus Cubes oder anderen Zellmengen ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-105">It is a collection of cells selected from cubes or other cellsets.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f0a-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3f0a-106">Remarks</span></span>

<span data-ttu-id="e3f0a-p102">Daten innerhalb einer Zellmenge werden per array-ähnlichem Direktzugriff abgerufen. Sie können einen Drilldown für ein bestimmtes Element ausführen, um Daten zu diesem Element abzurufen. Der folgende Code gibt beispielsweise die Beschriftung des ersten Elements in der ersten Position auf der ersten Achse der Zellmenge **cst** zurück:</span><span class="sxs-lookup"><span data-stu-id="e3f0a-p102">Data within a **Cellset** is retrieved using direct, array-like access. You can "drill down" to a specific member to obtain data about that member. For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named cst:</span></span>

`cst.Axes(0).Positions(0).Members(0).Caption`

<span data-ttu-id="e3f0a-p103">Innerhalb einer Zellmenge gibt es keine aktuelle Zelle. Stattdessen ruft die [Item](item-property-ado-md-cellset.md)-Eigenschaft ein bestimmtes [Cell](cell-object-ado-md.md)-Objekt aus der Zellmenge ab. Die Argumente der **Item** -Eigenschaft bestimmen, welche Zelle abgerufen wird. Sie können den eindeutigen Ordnungswert einer Zelle angeben. Sie können Zellen auch anhand ihrer Positionsnummern entlang der einzelnen Achsen in der Zellmenge abrufen. Weitere Informationen zum Abrufen von Zellen finden Sie im Thema zur [Item](item-property-ado-md-cellset.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-p103">There is no notion of a current cell within a cellset. Instead, the [Item](item-property-ado-md-cellset.md) property retrieves a specific [Cell](cell-object-ado-md.md) object from the cellset. The arguments of the **Item** property determine which cell is retrieved. You can specify the unique ordinal value of a cell. You can also retrieve cells by using their position numbers along each axis of the cellset. For more information about retrieving cells, see the [Item](item-property-ado-md-cellset.md) property.</span></span>

<span data-ttu-id="e3f0a-116">Die Auflistungen, Methoden und Eigenschaften eines **Cellset** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e3f0a-116">With the collections, methods, and properties of a **Cellset** object, you can do the following:</span></span>

  - <span data-ttu-id="e3f0a-117">Zuordnen einer geöffneten Verbindung zu einem **Cellset** -Objekt, indem dessen [ActiveConnection](activeconnection-property-ado-md.md)-Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-117">Associate an open connection with a **Cellset** object by setting its [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e3f0a-118">Ausführen einer multidimensionalen Abfrage und Abrufen der entsprechenden Ergebnisse, indem Sie die [Open](open-method-ado-md.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-118">Execute and retrieve the results of a multidimensional query with the [Open](open-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="e3f0a-119">Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-119">Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.</span></span>

  - <span data-ttu-id="e3f0a-120">Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-120">Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="e3f0a-121">Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-121">Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e3f0a-122">Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-122">Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e3f0a-123">Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-123">Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e3f0a-124">Close an open **Cellset** with the [Close](close-method-ado-md.md) method.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-124">Close an open **Cellset** with the [Close](close-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="e3f0a-125">Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-125">Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

