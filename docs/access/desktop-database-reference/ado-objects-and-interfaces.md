---
title: ADO-Objekte und -Schnittstellen
TOCTitle: ADO Objects and Interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efab7ce2980393282ee1f96295206e712fcbd15f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882182"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="2af81-102">ADO-Objekte und -Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2af81-102">ADO Objects and Interfaces</span></span>


<span data-ttu-id="2af81-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2af81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2af81-104">Die Beziehungen zwischen diesen Objekten werden im ADO-Objektmodell dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2af81-104">The relationships between these objects are represented in the ADO Object Model.</span></span>

<span data-ttu-id="2af81-p101">Jedes Objekt kann in der entsprechenden Auflistung enthalten sein. Beispielsweise kann ein [Error](error-object-ado.md)-Objekt in einer [Errors](errors-collection-ado.md)-Auflistung enthalten sein. Weitere Informationen finden Sie unter [ADO-Auflistungen](ado-collections.md) oder in einem auflistungsspezifischen Thema.</span><span class="sxs-lookup"><span data-stu-id="2af81-p101">Each object can be contained in its corresponding collection. For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection. For more information, see [ADO Collections](ado-collections.md) or a specific collection topic.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2af81-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="2af81-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="2af81-109">Ein <strong>Record</strong>-ADO-Objekt wird aus einem <strong>Row</strong>-OLE DB-Objekt in einer C/C++-Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="2af81-109">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2af81-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="2af81-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="2af81-111">Ein <strong>Recordset</strong>-ADO-Objekt wird aus einem <strong>Rowset</strong>-OLE DB-Objekt in einer C/C++-Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="2af81-111">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2af81-112"><a href="error-object-ado.md">Fehler</a></span><span class="sxs-lookup"><span data-stu-id="2af81-112"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="2af81-113">Enthält Details zu Datenzugriffsfehlern, die sich auf eine einzelne Operation beziehen, die den Anbieter betrifft.</span><span class="sxs-lookup"><span data-stu-id="2af81-113">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2af81-114"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="2af81-114"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="2af81-115">Stellt Daten mit einem gemeinsamen Datentyp in einer Spalte dar.</span><span class="sxs-lookup"><span data-stu-id="2af81-115">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2af81-116"><a href="parameter-object-ado.md">Parameter</a></span><span class="sxs-lookup"><span data-stu-id="2af81-116"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="2af81-117">Stellt einen Parameter oder ein Argument dar, der bzw. das einem <strong>Command</strong>-Objekt zugeordnet ist, das auf einer parametrisierten Abfrage oder einer gespeicherten Prozedur basiert.</span><span class="sxs-lookup"><span data-stu-id="2af81-117">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2af81-118"><a href="property-object-ado.md">Eigenschaft</a></span><span class="sxs-lookup"><span data-stu-id="2af81-118"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="2af81-119">Stellt ein dynamisches Merkmal eines ADO-Objekts dar, das vom Anbieter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="2af81-119">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2af81-120"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="2af81-120"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="2af81-121">Stellt eine Zeile eines <strong>Recordset</strong>-Objekts oder ein Verzeichnis oder eine Datei in einem Dateisystem dar.</span><span class="sxs-lookup"><span data-stu-id="2af81-121">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2af81-122"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="2af81-122"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="2af81-p102">Stellt den gesamten Satz der Datensätze aus einer Basistabelle oder die Ergebnisse eines ausgeführten Befehls dar. Das <strong>Recordset</strong> -Objekt verweist immer nur auf einen einzelnen Datensatz innerhalb des Satzes als aktueller Datensatz.</span><span class="sxs-lookup"><span data-stu-id="2af81-p102">Represents the entire set of records from a base table or the results of an executed command. At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2af81-125"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="2af81-125"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="2af81-126">Stellt einen binären Datenstrom dar.</span><span class="sxs-lookup"><span data-stu-id="2af81-126">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

