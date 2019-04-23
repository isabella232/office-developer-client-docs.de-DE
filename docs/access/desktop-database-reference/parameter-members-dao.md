---
title: Parameter-Elemente (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288112"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="8e2c7-102">Parameter-Elemente (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e2c7-102">Parameter members (DAO)</span></span>

<span data-ttu-id="8e2c7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e2c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e2c7-104">Ein Parameter-Objekt stellt einen Wert für eine Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-104">A Parameter object represents a value supplied to a query.</span></span> <span data-ttu-id="8e2c7-105">Der Parameter wird einem QueryDef-Objekt zugeordnet, das aus einer Parameterabfrage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-105">The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="8e2c7-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e2c7-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e2c7-107">Name</span><span class="sxs-lookup"><span data-stu-id="8e2c7-107">Name</span></span></p></th>
<th><p><span data-ttu-id="8e2c7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e2c7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e2c7-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span><span class="sxs-lookup"><span data-stu-id="8e2c7-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8e2c7-110"><strong>Hinweis</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-110"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8e2c7-111">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8e2c7-112">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob ein <strong><a href="parameter-object-dao.md">Parameter</a></strong> -Objekt einen Eingabeparameter und/oder einen Ausgabeparameter oder den Rückgabewert der Prozedur darstellt (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="8e2c7-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e2c7-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="8e2c7-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8e2c7-114">Gibt den Namen des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-114">Returns the name of the specified object.</span></span> <span data-ttu-id="8e2c7-115">Read-only <strong>Zeichenfolge</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-115">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e2c7-116"><strong><a href="parameter-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="8e2c7-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8e2c7-117">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-117">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="8e2c7-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-118">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e2c7-119"><strong><a href="parameter-type-property-dao.md">Typ</a></strong></span><span class="sxs-lookup"><span data-stu-id="8e2c7-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8e2c7-120">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-120">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="8e2c7-121"><strong>Integer</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-121">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e2c7-122"><strong><a href="parameter-value-property-dao.md">Wert</a></strong></span><span class="sxs-lookup"><span data-stu-id="8e2c7-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8e2c7-123">Legt den Wert eines Objekts fest oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-123">Sets or returns the value of an object.</span></span> <span data-ttu-id="8e2c7-124"><strong>Variant</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-124">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

