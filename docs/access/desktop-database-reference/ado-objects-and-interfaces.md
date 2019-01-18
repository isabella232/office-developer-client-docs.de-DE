---
title: ADO-Objekte und -Schnittstellen
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 539feb1918877189548d0e7cff6ceb28e50abddc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718861"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="5d05c-102">ADO-Objekte und -Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5d05c-102">ADO objects and interfaces</span></span>

<span data-ttu-id="5d05c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d05c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d05c-104">Die Beziehungen zwischen diesen Objekten werden im Objektmodell von ActiveX Data Objects (ADO) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5d05c-104">The relationships between these objects are represented in the ActiveX Data Objects (ADO) Object Model.</span></span>

<span data-ttu-id="5d05c-105">Jedes Objekt kann in der entsprechenden Auflistung enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="5d05c-105">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="5d05c-106">Beispielsweise kann ein [Error](error-object-ado.md)-Objekt in einer [Errors](errors-collection-ado.md)-Auflistung enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="5d05c-106">For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection.</span></span> <span data-ttu-id="5d05c-107">Weitere Informationen finden Sie unter [ADO-Auflistungen](ado-collections.md) oder einer bestimmten Sammlung Thema.</span><span class="sxs-lookup"><span data-stu-id="5d05c-107">For more information, see [ADO collections](ado-collections.md) or a specific collection topic.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="5d05c-108">Objekt</span><span class="sxs-lookup"><span data-stu-id="5d05c-108">Object</span></span></th>
<th><span data-ttu-id="5d05c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d05c-109">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d05c-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-111">Ein <strong>Record</strong>-ADO-Objekt wird aus einem <strong>Row</strong>-OLE DB-Objekt in einer C/C++-Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="5d05c-111">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d05c-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-113">Ein <strong>Recordset</strong>-ADO-Objekt wird aus einem <strong>Rowset</strong>-OLE DB-Objekt in einer C/C++-Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="5d05c-113">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d05c-114"><a href="error-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-114"><a href="error-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-115">Definiert einen spezifischen Befehl, den Sie in einer Datenquelle ausführen wollen.</span><span class="sxs-lookup"><span data-stu-id="5d05c-115">Defines a specific command that you intend to execute against a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d05c-116"><a href="field-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-116"><a href="field-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-117">Stellt eine offene Verbindung zu einer Datenquelle dar.</span><span class="sxs-lookup"><span data-stu-id="5d05c-117">Represents an open connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d05c-118"><a href="error-object-ado.md">Fehler</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-118"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-119">Enthält Details zu Datenzugriffsfehlern, die sich auf eine einzelne Operation beziehen, die den Anbieter betrifft.</span><span class="sxs-lookup"><span data-stu-id="5d05c-119">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d05c-120"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-120"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-121">Stellt Daten mit einem gemeinsamen Datentyp in einer Spalte dar.</span><span class="sxs-lookup"><span data-stu-id="5d05c-121">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d05c-122"><a href="parameter-object-ado.md">Parameter</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-122"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-123">Stellt einen Parameter oder ein Argument dar, der bzw. das einem <strong>Command</strong>-Objekt zugeordnet ist, das auf einer parametrisierten Abfrage oder einer gespeicherten Prozedur basiert.</span><span class="sxs-lookup"><span data-stu-id="5d05c-123">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d05c-124"><a href="property-object-ado.md">Eigenschaft</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-124"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-125">Stellt ein dynamisches Merkmal eines ADO-Objekts dar, das vom Anbieter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="5d05c-125">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d05c-126"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-126"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-127">Stellt eine Zeile eines <strong>Recordset</strong>-Objekts oder ein Verzeichnis oder eine Datei in einem Dateisystem dar.</span><span class="sxs-lookup"><span data-stu-id="5d05c-127">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d05c-128"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-128"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-p102">Stellt den gesamten Satz der Datensätze aus einer Basistabelle oder die Ergebnisse eines ausgeführten Befehls dar. Das <strong>Recordset</strong> -Objekt verweist immer nur auf einen einzelnen Datensatz innerhalb des Satzes als aktueller Datensatz.</span><span class="sxs-lookup"><span data-stu-id="5d05c-p102">Represents the entire set of records from a base table or the results of an executed command. At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d05c-131"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="5d05c-131"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="5d05c-132">Stellt einen binären Datenstrom dar.</span><span class="sxs-lookup"><span data-stu-id="5d05c-132">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

