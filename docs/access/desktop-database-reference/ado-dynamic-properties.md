---
title: Dynamische ADO-Eigenschaften
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fae0df2a4cc5c9de585d2b101e9fa31cb6a0a545
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714521"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="6be25-102">Dynamische ADO-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6be25-102">ADO dynamic properties</span></span>

<span data-ttu-id="6be25-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6be25-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6be25-p101">Dynamische Eigenschaften können den [Properties](properties-collection-ado.md)-Auflistungen der [Connection](connection-object-ado.md)-, [Command](command-object-ado.md)- oder [Recordset](recordset-object-ado.md)-Objekte hinzugefügt werden. Die Quelle für diese Eigenschaften ist ein Datenanbieter, wie z. B. der [OLE DB-Anbieter für SQL Server](microsoft-ole-db-provider-for-sql-server.md), oder ein Dienstanbieter, wie z. B. der [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Weitere Informationen zu einer bestimmten dynamischen Eigenschaft finden Sie in der Dokumentation des entsprechenden Datenanbieters oder Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="6be25-p101">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects. The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="6be25-107">Der [Dynamische ADO-Eigenschaftenindex](ado-dynamic-property-index.md) stellt einen Querverweis zwischen den ADO- und OLE DB-Namen der einzelnen dynamischen Standardeigenschaften des OLE DB-Anbieters bereit.</span><span class="sxs-lookup"><span data-stu-id="6be25-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="6be25-p102">Die folgenden dynamischen Eigenschaften sind von besonderem Interesse und werden ebenfalls in den oben genannten Quellen dokumentiert. Die spezielle Funktionalität mit ADO ist in den unten aufgelisteten ADO-Hilfethemen dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="6be25-p102">The following dynamic properties are of special interest, and are also documented in the sources mentioned above. Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="6be25-110">Dynamische Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6be25-110">Dynamic property</span></span></th>
<th><span data-ttu-id="6be25-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6be25-111">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be25-112"><a href="optimize-property-dynamic-ado.md">Optimieren der Leistung von</a></span><span class="sxs-lookup"><span data-stu-id="6be25-112"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="6be25-113">Es wird angegeben, ob für dieses Feld ein Index erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6be25-113">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be25-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span><span class="sxs-lookup"><span data-stu-id="6be25-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="6be25-115">Gibt an, ob der OLE DB-Anbieter den Benutzer zur Eingabe von Initialisierungsinformationen auffordern soll.</span><span class="sxs-lookup"><span data-stu-id="6be25-115">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be25-116"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="6be25-116"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="6be25-117">Gibt einen Namen für das <strong>Recordset</strong>-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6be25-117">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be25-118"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="6be25-118"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="6be25-119">Gibt eine vom Benutzer bereitgestellte Befehlszeichenfolge an, die von der <strong>Resync</strong>-Methode ausgegeben wird, um die Daten in der Tabelle zu aktualisieren, die in der dynamischen <strong>Unique Table</strong>-Eigenschaft genannt ist.</span><span class="sxs-lookup"><span data-stu-id="6be25-119">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be25-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="6be25-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="6be25-121"><strong>Unique Table</strong> – gibt den Namen der Basistabelle, für das Aktualisierungen, einfügungen und Löschvorgänge zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6be25-121"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span><br/><br/><span data-ttu-id="6be25-122"><strong>Unique Schema</strong> – gibt an, das Schema oder der Name des Besitzers der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6be25-122"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span><br/><br/><span data-ttu-id="6be25-123"><strong>Unique Catalog</strong> – gibt den Katalog oder Name der Datenbank, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="6be25-123"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be25-124"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span><span class="sxs-lookup"><span data-stu-id="6be25-124"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="6be25-125">Gibt an, ob auf die <strong>UpdateBatch</strong>-Methode ein impliziter Vorgang mit einer <strong>Resync</strong>-Methode folgt. Wenn dies der Fall ist, wird der Bereich des Vorgangs angegeben.</span><span class="sxs-lookup"><span data-stu-id="6be25-125">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

