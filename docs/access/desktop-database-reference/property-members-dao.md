---
title: Eigenschaftselemente (DAO)
TOCTitle: Property Members
ms:assetid: 32658adb-f153-148d-a216-eb97b996579a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192303(v=office.15)
ms:contentKeyID: 48544076
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe60c12a85eff0dd8f796f9affeef71979dac580
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301211"
---
# <a name="property-members-dao"></a><span data-ttu-id="92ec0-102">Eigenschaftselemente (DAO)</span><span class="sxs-lookup"><span data-stu-id="92ec0-102">Property members (DAO)</span></span>


<span data-ttu-id="92ec0-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92ec0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92ec0-104">Ein Property-Objekt stellt eine integrierte oder benutzerdefinierte Eigenschaft eines DAO-Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="92ec0-104">A Property object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="properties"></a><span data-ttu-id="92ec0-105">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92ec0-105">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92ec0-106">Name</span><span class="sxs-lookup"><span data-stu-id="92ec0-106">Name</span></span></p></th>
<th><p><span data-ttu-id="92ec0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92ec0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92ec0-108"><strong><a href="property-inherited-property-dao.md">Vererbt</a></strong></span><span class="sxs-lookup"><span data-stu-id="92ec0-108"><strong><a href="property-inherited-property-dao.md">Inherited</a></strong></span></span></p></td>
<td><p><span data-ttu-id="92ec0-109">Gibt einen Wert zurück, der angibt, ob ein <strong><a href="property-object-dao.md">Property</a></strong> -Objekt von einem zugrunde liegenden Objekt geerbt wurde.</span><span class="sxs-lookup"><span data-stu-id="92ec0-109">Returns a value that indicates whether a <strong><a href="property-object-dao.md">Property</a></strong> object is inherited from an underlying object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92ec0-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="92ec0-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="92ec0-p101">Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff, wenn das Objekt noch keiner Auflistung angefügt wurde. Schreibgeschützter <strong>String</strong>-Wert, wenn das Objekt einer Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="92ec0-p101">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92ec0-114"><strong><a href="property-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="92ec0-114"><strong><a href="property-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="92ec0-115">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="92ec0-115">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="92ec0-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="92ec0-116">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92ec0-117"><strong><a href="property-type-property-dao.md">Typ</a></strong></span><span class="sxs-lookup"><span data-stu-id="92ec0-117"><strong><a href="property-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="92ec0-118">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="92ec0-118">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="92ec0-119"><strong>Integer</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="92ec0-119">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92ec0-120"><strong><a href="property-value-property-dao.md">Wert</a></strong></span><span class="sxs-lookup"><span data-stu-id="92ec0-120"><strong><a href="property-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="92ec0-121">Legt den Wert eines Objekts fest oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="92ec0-121">Sets or returns the value of an object.</span></span> <span data-ttu-id="92ec0-122"><strong>Variant</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="92ec0-122">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

