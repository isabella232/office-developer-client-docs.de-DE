---
title: Document-Elemente (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd50ec72113b0615849ff6b8b2e8d73c0e61c3ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293791"
---
# <a name="document-members-dao"></a><span data-ttu-id="a40e2-102">Document-Elemente (DAO)</span><span class="sxs-lookup"><span data-stu-id="a40e2-102">Document members (DAO)</span></span>


<span data-ttu-id="a40e2-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a40e2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a40e2-p101">Ein Document-Objekt schließt Informationen zu einer Objektinstanz ein. Bei dem Objekt kann es sich um eine Datenbank, gespeicherte Tabelle, Abfrage oder Beziehung handeln (gilt nur für Microsoft Access-Datenbanken).</span><span class="sxs-lookup"><span data-stu-id="a40e2-p101">A Document object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="a40e2-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="a40e2-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a40e2-107">Name</span><span class="sxs-lookup"><span data-stu-id="a40e2-107">Name</span></span></p></th>
<th><p><span data-ttu-id="a40e2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a40e2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a40e2-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="a40e2-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a40e2-110">Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a40e2-110">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="a40e2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a40e2-111">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a40e2-112">Name</span><span class="sxs-lookup"><span data-stu-id="a40e2-112">Name</span></span></p></th>
<th><p><span data-ttu-id="a40e2-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a40e2-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a40e2-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span><span class="sxs-lookup"><span data-stu-id="a40e2-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a40e2-115">Gibt den Namen des <strong><a href="container-object-dao.md">Container</a></strong> -Objekts zurück, zu dem ein <strong>Document</strong> -Objekt gehört (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a40e2-115">Returns the name of the <strong><a href="container-object-dao.md">Container</a></strong> object to which a <strong>Document</strong> object belongs (Microsoft Access workspaces only).</span></span> <span data-ttu-id="a40e2-116">.</span><span class="sxs-lookup"><span data-stu-id="a40e2-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a40e2-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="a40e2-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a40e2-118">Gibt das Datum und die Uhrzeit zurück, zu der ein Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a40e2-118">Returns the date and time that an object was created.</span></span> <span data-ttu-id="a40e2-119">Read-only <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="a40e2-119">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a40e2-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="a40e2-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a40e2-121">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="a40e2-121">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="a40e2-122">Schreibgeschützter <strong>Variant</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="a40e2-122">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a40e2-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="a40e2-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a40e2-124">Gibt den Namen des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="a40e2-124">Returns the name of the specified object.</span></span> <span data-ttu-id="a40e2-125">Read-only <strong>Zeichenfolge</strong>.</span><span class="sxs-lookup"><span data-stu-id="a40e2-125">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a40e2-126"><strong><a href="document-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="a40e2-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a40e2-127">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="a40e2-127">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="a40e2-128">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a40e2-128">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

