---
title: Members-Auflistung (ADO MD)
TOCTitle: Members Collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7142c65bba1df724125c66928001c2b3cd71f1b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876393"
---
# <a name="members-collection-ado-md"></a><span data-ttu-id="79c86-102">Members-Auflistung (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="79c86-102">Members Collection (ADO MD)</span></span>


<span data-ttu-id="79c86-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79c86-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79c86-104">Enthält die[Member](member-object-ado-md.md)-Objekte einer Ebene oder einer Position entlang einer Achse.</span><span class="sxs-lookup"><span data-stu-id="79c86-104">Contains the [Member](member-object-ado-md.md) objects from a level or a position along an axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="79c86-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="79c86-105">Remarks</span></span>

<span data-ttu-id="79c86-106">Eine **Members** -Auflistung kann die folgenden Elementtypen enthalten:</span><span class="sxs-lookup"><span data-stu-id="79c86-106">A **Members** collection is used to contain the following types of members:</span></span>

  - <span data-ttu-id="79c86-p101">Die Elemente, die eine Ebene in einem Cube bilden. Sie sind in der Members-Auflistung eines Level-Objekts enthalten. Im Beispiel aus Übersicht über Multidimensionale Schemas und Daten stellen Canada, USA, UK und Germany die vier Elemente der Länderebene dar.</span><span class="sxs-lookup"><span data-stu-id="79c86-p101">The members that make up a level in a cube. These are contained in the **Members** collection of a [Level](level-object-ado-md.md) object. For example, using the sample from [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md), the four members of the Countries level are Canada, USA, UK, and Germany.</span></span>

  - <span data-ttu-id="79c86-p102">Die Elemente, die die untergeordneten Elemente eines bestimmten Elements in einer Hierarchie darstellen. Diese Elemente werden von der [Children](children-property-ado-md.md)-Eigenschaft des übergeordneten **Member** -Objekts zurückgegeben. In demselben Beispiel sind Canada-East und Canada-West die beiden Elemente, die dem Element Canada untergeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="79c86-p102">The members that are the children of a specific member within a hierarchy. These members are returned by the [Children](children-property-ado-md.md) property of the parent **Member** object. For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</span></span>

  - <span data-ttu-id="79c86-p103">Die Elemente, die eine bestimmte Position entlang der Achse einer Zellmenge definieren. Im Beispiel aus Verwenden von multidimensionalen Daten stellen Valentine und Seattle die beiden Elemente der ersten Position auf der X-Achse dar. Diese Elemente sind in der Members-Auflistung eines Position-Objekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="79c86-p103">The members that define a specific position along an axis of a [cellset](cellset-object-ado-md.md). Using the cellset from [Working with Multidimensional Data](working-with-multidimensional-data.md) as an example, the two members of the first position on the x-axis are Valentine and Seattle. These members are contained by the **Members** collection of a [Position](position-object-ado-md.md) object.</span></span>

<span data-ttu-id="79c86-p104">**Members** ist eine ADO-Standardauflistung. Die Eigenschaften und Methoden einer Auflistung ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="79c86-p104">**Members** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="79c86-118">Abrufen der Anzahl an Objekten in der Auflistung, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="79c86-118">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="79c86-119">Zurückgeben eines Objekts aus der Auflistung, indem Sie die Standardeigenschaft [Item](item-property-ado.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="79c86-119">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="79c86-120">Aktualisieren der Objekte in der Auflistung aus dem Anbieter, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="79c86-120">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

