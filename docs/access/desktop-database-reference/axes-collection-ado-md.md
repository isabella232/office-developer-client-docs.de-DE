---
title: Axes-Auflistung (ADO MD)
TOCTitle: Axes Collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2b078f2d8f1ea6562d6f82f90943923c7d92a07
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475181"
---
# <a name="axes-collection-ado-md"></a><span data-ttu-id="306a6-102">Axes-Auflistung (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="306a6-102">Axes Collection (ADO MD)</span></span>


<span data-ttu-id="306a6-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="306a6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="306a6-104">Enthält die [Axis](axis-object-ado-md.md)-Objekte, die eine Zellmenge definieren.</span><span class="sxs-lookup"><span data-stu-id="306a6-104">Contains the [Axis](axis-object-ado-md.md) objects that define a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="306a6-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="306a6-105">Remarks</span></span>

<span data-ttu-id="306a6-p101">Ein [Cellset](cellset-object-ado-md.md)-Objekt enthält eine **Axes** -Auflistung. Nach dem Öffnen des **Cellset** -Objekts enthält diese Auflistung mindestens ein **Axis** -Objekt. Eine ausführlichere Erläuterung zum Verwenden von [Axis](axis-object-ado-md.md) -Objekten finden Sie im Thema zum **Axis**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="306a6-p101">A [Cellset](cellset-object-ado-md.md) object contains an **Axes** collection. Once the **Cellset** is opened, this collection will contain at least one **Axis**. See the [Axis](axis-object-ado-md.md) object for a more detailed explanation of how to use **Axis** objects.</span></span>


> [!NOTE]
> <P><span data-ttu-id="306a6-p102">[!HINWEIS] Die Filterachse eines <STRONG>Cellset</STRONG> -Objekts ist nicht in der <STRONG>Axes</STRONG> -Auflistung enthalten. Weitere Informationen finden Sie im Thema zur <A href="filteraxis-property-ado-md.md">FilterAxis</A>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="306a6-p102">The filter axis of a <STRONG>Cellset</STRONG> is not contained in the <STRONG>Axes</STRONG> collection. See the <A href="filteraxis-property-ado-md.md">FilterAxis</A> property for more information.</span></span></P>



<span data-ttu-id="306a6-p103">**Axes** ist eine ADO-Standardauflistung. Die Eigenschaften und Methoden einer Auflistung ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="306a6-p103">**Axes** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="306a6-113">Abrufen der Anzahl an Objekten in der Auflistung, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="306a6-113">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="306a6-114">Zurückgeben eines Objekts aus der Auflistung, indem Sie die Standardeigenschaft [Item](item-property-ado.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="306a6-114">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="306a6-115">Aktualisieren der Objekte in der Auflistung aus dem Anbieter, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="306a6-115">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

