---
title: Catalog-Objekt (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b977db2faf07a47c2e9234cec4a7828def5e6188
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926738"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="ca76f-102">Catalog-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ca76f-102">Catalog object (ADO MD)</span></span>


<span data-ttu-id="ca76f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca76f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca76f-104">Enthält multidimensionale Schemainformationen (Cubes und zugrunde liegende Dimensionen, Hierarchien, Ebenen und Elemente), die für einen multidimensionalen Datenanbieter (Datenprovider, MDP) spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="ca76f-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca76f-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca76f-105">Remarks</span></span>

<span data-ttu-id="ca76f-106">Die Auflistungen und Eigenschaften eines **Catalog** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ca76f-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

  - <span data-ttu-id="ca76f-107">Öffnen des Katalogs, indem Sie für die [ActiveConnection](activeconnection-property-ado-md.md)-Eigenschaft ein [Connection](connection-object-ado.md)-ADO-Standardobjekt oder eine gültige Verbindungszeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="ca76f-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

  - <span data-ttu-id="ca76f-108">Identifizieren des\*\*\*\* Katalogs, indem Sie die [Name](name-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca76f-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="ca76f-109">Durchlaufen der Cubes in einem Katalog, indem Sie die [CubeDefs](cubedefs-collection-ado-md.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca76f-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

