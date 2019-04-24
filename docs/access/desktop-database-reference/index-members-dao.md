---
title: Index Elemente (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291796"
---
# <a name="index-members-dao"></a><span data-ttu-id="c2e96-102">Index Elemente (DAO)</span><span class="sxs-lookup"><span data-stu-id="c2e96-102">Index members (DAO)</span></span>


<span data-ttu-id="c2e96-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2e96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2e96-p101">Index-Objekte geben die Reihenfolge an, in der auf Datensätze aus Datenbanktabellen zugegriffen wird, und sie geben an, ob doppelte Datensätze akzeptiert werden. Dadurch stellen sie einen effizienten Zugriff auf Daten sicher. Bei externen Datenbanken beschreiben Index-Objekte die für externe Tabellen eingerichteten Indizes (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c2e96-p101">Index objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, Index objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="c2e96-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="c2e96-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2e96-107">Name</span><span class="sxs-lookup"><span data-stu-id="c2e96-107">Name</span></span></p></th>
<th><p><span data-ttu-id="c2e96-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2e96-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2e96-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-110">Erstellt ein neues <strong><a href="field-object-dao.md">Field</a></strong> -Objekt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c2e96-110">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2e96-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-112">Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c2e96-112">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="c2e96-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2e96-113">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2e96-114">Name</span><span class="sxs-lookup"><span data-stu-id="c2e96-114">Name</span></span></p></th>
<th><p><span data-ttu-id="c2e96-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2e96-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2e96-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-p102">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ab ein <strong>Index</strong>-Objekt einen gruppierten Index für eine Tabelle darstellt (gilt nur für Microsoft Access-Arbeitsbereiche). <strong>Boolean</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c2e96-p102">Sets or returns a value that indicates whether an <strong>Index</strong> object represents a clustered index for a table (Microsoft Access workspaces only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2e96-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-120">Gibt einen Wert zurück, der die Anzahl von eindeutigen, in der verknüpften Tabelle eingeschlossen Werten für das <strong><a href="index-object-dao.md">Index</a></strong> -Objekt angibt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c2e96-120">Returns a value that indicates the number of unique values for the <strong><a href="index-object-dao.md">Index</a></strong> object that are included in the associated table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2e96-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-122">Gibt eine <strong>Fields</strong>-Auflistung zurück, die alle gespeicherten <strong>Field</strong>-Objekte für das angegebene Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="c2e96-122">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="c2e96-123">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c2e96-123">Read/write.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2e96-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-125">Gibt einen Wert zurück, der angibt, ob ein <strong><a href="index-object-dao.md">Index</a></strong> -Objekt einen Fremdschlüssel in einer Tabelle darstellt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c2e96-125">Returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a foreign key in a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="c2e96-126">.</span><span class="sxs-lookup"><span data-stu-id="c2e96-126"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2e96-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-128">Legt einen Wert fest, der angibt, ob Datensätze, deren Indexfelder Nullwerte enthalten, über Indexeinträge verfügen (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c2e96-128">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2e96-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-p105">Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff, wenn das Objekt noch keiner Auflistung angefügt wurde. Schreibgeschützter <strong>String</strong>-Wert, wenn das Objekt einer Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c2e96-p105">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2e96-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-134">Legt einen Wert fest, der angibt, ob ein <strong><a href="index-object-dao.md">Index</a></strong> -Objekt einen Primärschlüsselindex für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c2e96-134">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a primary key index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2e96-135"><strong><a href="index-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-136">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="c2e96-136">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="c2e96-137">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c2e96-137">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2e96-138"><strong><a href="index-required-property-dao.md">Erforderlich</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-138"><strong><a href="index-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-139">Gibt einen Wert zurück, der angibt, ob für ein <strong><a href="field-object-dao.md">Field</a></strong> -Objekt ein Nicht-Null-Wert erforderlich ist, oder legt den betreffenden Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c2e96-139">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2e96-140"><strong><a href="index-unique-property-dao.md">Eigen</a></strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-141">Legt einen Wert fest, der angibt, ob ein <strong><a href="index-object-dao.md">Index</a></strong> -Objekt einen eindeutigen Index (Schlüssel) für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c2e96-141">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

