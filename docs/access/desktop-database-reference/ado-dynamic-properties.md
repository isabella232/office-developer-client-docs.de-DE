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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281715"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="f4097-102">Dynamische ADO-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4097-102">ADO dynamic properties</span></span>

<span data-ttu-id="f4097-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4097-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4097-p101">Dynamische Eigenschaften können den [Properties](properties-collection-ado.md)-Auflistungen der [Connection](connection-object-ado.md)-, [Command](command-object-ado.md)- oder [Recordset](recordset-object-ado.md)-Objekte hinzugefügt werden. Die Quelle für diese Eigenschaften ist ein Datenanbieter, wie z. B. der [OLE DB-Anbieter für SQL Server](microsoft-ole-db-provider-for-sql-server.md), oder ein Dienstanbieter, wie z. B. der [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Weitere Informationen zu einer bestimmten dynamischen Eigenschaft finden Sie in der Dokumentation des entsprechenden Datenanbieters oder Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="f4097-p101">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects. The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="f4097-107">Der [Dynamische ADO-Eigenschaftenindex](ado-dynamic-property-index.md) stellt einen Querverweis zwischen den ADO- und OLE DB-Namen der einzelnen dynamischen Standardeigenschaften des OLE DB-Anbieters bereit.</span><span class="sxs-lookup"><span data-stu-id="f4097-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="f4097-p102">Die folgenden dynamischen Eigenschaften sind von besonderem Interesse und werden ebenfalls in den oben genannten Quellen dokumentiert. Die spezielle Funktionalität mit ADO ist in den unten aufgelisteten ADO-Hilfethemen dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="f4097-p102">The following dynamic properties are of special interest, and are also documented in the sources mentioned above. Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="f4097-110">Dynamic-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f4097-110">Dynamic property</span></span></th>
<th><span data-ttu-id="f4097-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4097-111">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4097-112"><a href="optimize-property-dynamic-ado.md">Optimieren</a></span><span class="sxs-lookup"><span data-stu-id="f4097-112"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="f4097-113">Es wird angegeben, ob für dieses Feld ein Index erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4097-113">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4097-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span><span class="sxs-lookup"><span data-stu-id="f4097-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="f4097-115">Es wird angegeben, ob der OLE DB-Anbieter den Benutzer zur Angabe von Initialisierungsinformationen auffordern sollte.</span><span class="sxs-lookup"><span data-stu-id="f4097-115">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4097-116"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="f4097-116"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="f4097-117">Es wird ein Name für das <strong>Recordset</strong>-Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="f4097-117">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4097-118"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="f4097-118"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="f4097-119">Es wird eine vom Benutzer bereitgestellte Befehlszeichenfolge angegeben, die von der <strong>Resync</strong>-Methode ausgegeben wird, um die Daten in der Tabelle, die in der dynamischen <strong>Unique Table</strong>-Eigenschaft genannt ist, zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f4097-119">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4097-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="f4097-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="f4097-121"><strong>Unique Table</strong> – gibt den Namen der Basistabelle an, für die Aktualisierungen, Einfügungen und Löschungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f4097-121"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span><br/><br/><span data-ttu-id="f4097-122"><strong>Unique Schema</strong> – gibt das Schema oder den Namen des Besitzers der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="f4097-122"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span><br/><br/><span data-ttu-id="f4097-123"><strong>EindeutigEr Katalog</strong> -gibt den Katalog oder den Namen der Datenbank an, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="f4097-123"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4097-124"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span><span class="sxs-lookup"><span data-stu-id="f4097-124"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="f4097-125">Es wird angegeben, ob auf die <strong>UpdateBatch</strong>-Methode eine implizite <strong>Resync</strong>-Methodenoperation folgt, und es wird gegebenenfalls der Umfang der Operation angegeben.</span><span class="sxs-lookup"><span data-stu-id="f4097-125">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

