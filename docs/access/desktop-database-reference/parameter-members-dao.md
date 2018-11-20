---
title: Parameter-Member (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e62125ee61598d6be125f9edb01f2aa4531043b9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026071"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="c9015-102">Parameter-Member (DAO)</span><span class="sxs-lookup"><span data-stu-id="c9015-102">Parameter members (DAO)</span></span>

<span data-ttu-id="c9015-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9015-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9015-p101">Ein Parameter-Objekt stellt einen Wert für eine Abfrage dar. Der Parameter wird einem QueryDef-Objekt zugeordnet, das aus einer Parameterabfrage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c9015-p101">A Parameter object represents a value supplied to a query. The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="c9015-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9015-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9015-107">Name</span><span class="sxs-lookup"><span data-stu-id="c9015-107">Name</span></span></p></th>
<th><p><span data-ttu-id="c9015-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9015-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9015-109"><strong><a href="parameter-direction-property-dao.md"><ui>Direction</ui></a></strong></span><span class="sxs-lookup"><span data-stu-id="c9015-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c9015-110"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9015-110"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c9015-111">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9015-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c9015-112">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob ein <strong><a href="parameter-object-dao.md">Parameter</a></strong> -Objekt einen Eingabeparameter und/oder einen Ausgabeparameter oder den Rückgabewert der Prozedur darstellt (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c9015-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9015-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="c9015-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c9015-p103">Gibt den Namen des angegebenen Objekts zurück. Schreibgeschützter <strong>String</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="c9015-p103">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9015-116"><strong><a href="parameter-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="c9015-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c9015-p104">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c9015-p104">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9015-119"><strong><a href="parameter-type-property-dao.md">Typ</a></strong></span><span class="sxs-lookup"><span data-stu-id="c9015-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c9015-p105">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff <strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9015-p105">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9015-122"><strong><a href="parameter-value-property-dao.md">Wert</a></strong></span><span class="sxs-lookup"><span data-stu-id="c9015-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c9015-p106">Legt den Wert eines Objekts fest oder gibt ihn zurück. <strong>Variant</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c9015-p106">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

