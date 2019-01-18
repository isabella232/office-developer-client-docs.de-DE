---
title: SchemaEnum (Access PC-Datenbank-Referenz)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718826"
---
# <a name="schemaenum"></a><span data-ttu-id="ad686-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="ad686-102">SchemaEnum</span></span>

<span data-ttu-id="ad686-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad686-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad686-104">Der Typ des **Recordset** -Schemaobjekts wird angegeben, das von der [OpenSchema](openschema-method-ado.md)-Methode abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ad686-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad686-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad686-105">Remarks</span></span>

<span data-ttu-id="ad686-106">Weitere Informationen über die Funktion und den Spalten, die für jede ADO-Konstante zurückgegeben finden Sie in den Themen von Anhang B der *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="ad686-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="ad686-107">Die Namen der einzelnen Themen wird in Klammern im Abschnitt Beschreibung in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad686-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="ad686-108">Weitere Informationen über die Funktion und den Spalten, die für jede ADO MD-Konstante zurückgegeben finden Sie in Kapitel 23 der Dokumentation zu *OLE DB für OLAP* .</span><span class="sxs-lookup"><span data-stu-id="ad686-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="ad686-109">Die Namen der einzelnen Themen, die in Klammern aufgelistet und mit einem Sternchen gekennzeichnet ist (\*) in der Spalte Beschreibung in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ad686-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="ad686-110">Übersetzen Sie die Datentypen der Spalten in der Dokumentation zu OLE DB in ADO-Datentypen anhand der Spalte Beschreibung des Themas ADO [DataTypeEnum-Wert](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="ad686-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="ad686-111">Angenommen, ein OLE DB-Datentyp des **DATENBANKTYP\_WSTR** ein ADO-Datentyp des **AdWChar**entspricht.</span><span class="sxs-lookup"><span data-stu-id="ad686-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="ad686-112">ADO generiert Schema-ähnliche Ergebnisse für die Konstanten, die **AdSchemaDBInfoKeywords** und **AdSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="ad686-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="ad686-113">ADO ein **Recordset-Objekt**erstellt, und füllt dann jede Zeile mit den Werten, die von den Methoden **IDBInfo:: GetKeywords** und **:: GetLiteralInfo** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad686-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="ad686-114">Weitere Informationen zu diesen Methoden finden Sie im Abschnitt "IDBInfo" der *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="ad686-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad686-115">Konstante</span><span class="sxs-lookup"><span data-stu-id="ad686-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="ad686-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ad686-116">Value</span></span></p></th>
<th><p><span data-ttu-id="ad686-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad686-117">Description</span></span></p></th>
<th><p><span data-ttu-id="ad686-118">Einschränkungsspalten</span><span class="sxs-lookup"><span data-stu-id="ad686-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad686-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-120">0</span><span class="sxs-lookup"><span data-stu-id="ad686-120">0</span></span></p></td>
<td><p><span data-ttu-id="ad686-121">Gibt die im Katalog definierten Assertionen zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="ad686-122">(ASSERTIONS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="ad686-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="ad686-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-127">1</span><span class="sxs-lookup"><span data-stu-id="ad686-127">1</span></span></p></td>
<td><p><span data-ttu-id="ad686-128">Gibt die physikalischen Attribute zurück, die Katalogen zugeordnet sind, auf die vom DBMS zugegriffen werden kann.
</span><span class="sxs-lookup"><span data-stu-id="ad686-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="ad686-129">(CATALOGS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-132">2</span><span class="sxs-lookup"><span data-stu-id="ad686-132">2</span></span></p></td>
<td><p><span data-ttu-id="ad686-133">Gibt die im Katalog definierten Zeichensätze zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="ad686-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="ad686-134">(CHARACTER_SETS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="ad686-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="ad686-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-139">5</span><span class="sxs-lookup"><span data-stu-id="ad686-139">5</span></span></p></td>
<td><p><span data-ttu-id="ad686-140">Gibt die im Katalog definierten CHECK-Einschränkungen zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="ad686-141">(CHECK_CONSTRAINTS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="ad686-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="ad686-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-146">3</span><span class="sxs-lookup"><span data-stu-id="ad686-146">3</span></span></p></td>
<td><p><span data-ttu-id="ad686-147">Gibt die im Katalog definierten Sortierungen zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="ad686-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="ad686-148">(COLLATIONS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="ad686-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="ad686-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-153">13</span><span class="sxs-lookup"><span data-stu-id="ad686-153">13</span></span></p></td>
<td><p><span data-ttu-id="ad686-154">Gibt die im Katalog definierten Tabellenspaltenberechtigungen zurück, die einem bestimmten Benutzer zur Verfügung stehen oder von diesem erteilt werden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="ad686-155">(COLUMN_PRIVILEGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-158">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-158">TABLE_NAME</span></span><br />
<span data-ttu-id="ad686-159">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="ad686-160">RECHTEFÜR</span><span class="sxs-lookup"><span data-stu-id="ad686-160">GRANTOR</span></span><br />
<span data-ttu-id="ad686-161">BERECHTIGTE</span><span class="sxs-lookup"><span data-stu-id="ad686-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-162"><strong>"adSchemaColumns"</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-163">4</span><span class="sxs-lookup"><span data-stu-id="ad686-163">4</span></span></p></td>
<td><p><span data-ttu-id="ad686-164">Gibt die im Katalog definierten Tabellenspalten (einschließlich Sichten) zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="ad686-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="ad686-165">(COLUMNS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-168">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-168">TABLE_NAME</span></span><br />
<span data-ttu-id="ad686-169">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-171">11</span><span class="sxs-lookup"><span data-stu-id="ad686-171">11</span></span></p></td>
<td><p><span data-ttu-id="ad686-172">Gibt die im Katalog definierten Spalten zurück, die von einer im Katalog definierten Domäne abhängig sind und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="ad686-173">(COLUMN_DOMAIN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="ad686-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="ad686-176">DOMÄNENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="ad686-177">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-179">6</span><span class="sxs-lookup"><span data-stu-id="ad686-179">6</span></span></p></td>
<td><p><span data-ttu-id="ad686-180">Gibt die im Katalog definierten Spalten zurück, die von referenziellen Einschränkungen, eindeutigen Einschränkungen, CHECK-Einschränkungen und Assertionen verwendet werden und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="ad686-181">(CONSTRAINT_COLUMN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-184">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-184">TABLE_NAME</span></span><br />
<span data-ttu-id="ad686-185">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-187">7</span><span class="sxs-lookup"><span data-stu-id="ad686-187">7</span></span></p></td>
<td><p><span data-ttu-id="ad686-188">Gibt die im Katalog definierten Tabellen zurück, die von referenziellen Einschränkungen, eindeutigen Einschränkungen, CHECK-Einschränkungen und Assertionen verwendet werden und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="ad686-189">(CONSTRAINT_TABLE_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-192">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-194">32</span><span class="sxs-lookup"><span data-stu-id="ad686-194">32</span></span></p></td>
<td><p><span data-ttu-id="ad686-195">Gibt Informationen zu den verfügbaren Cubes in einem Schema zurück (oder im Katalog, wenn der Anbieter keine Schemas unterstützt).
</span><span class="sxs-lookup"><span data-stu-id="ad686-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="ad686-196">(CUBES-Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="ad686-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="ad686-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="ad686-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="ad686-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-201">30</span><span class="sxs-lookup"><span data-stu-id="ad686-201">30</span></span></p></td>
<td><p><span data-ttu-id="ad686-202">Gibt eine Liste anbieterspezifischer Schlüsselwörter zurück.
</span><span class="sxs-lookup"><span data-stu-id="ad686-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="ad686-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="ad686-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="ad686-204">&lt;None&gt;</span><span class="sxs-lookup"><span data-stu-id="ad686-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-206">31</span><span class="sxs-lookup"><span data-stu-id="ad686-206">31</span></span></p></td>
<td><p><span data-ttu-id="ad686-207">Gibt eine Liste anbieterspezifischer Literale zurück, die in Textbefehlen verwendet werden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="ad686-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="ad686-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="ad686-209">&lt;None&gt;</span><span class="sxs-lookup"><span data-stu-id="ad686-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-211">33</span><span class="sxs-lookup"><span data-stu-id="ad686-211">33</span></span></p></td>
<td><p><span data-ttu-id="ad686-212">Gibt Informationen zu den Dimensionen in einem bestimmten Cube zurück.</span><span class="sxs-lookup"><span data-stu-id="ad686-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="ad686-213">Es wurde eine Zeile für jede Dimension.</span><span class="sxs-lookup"><span data-stu-id="ad686-213">It has one row for each dimension.</span></span> <span data-ttu-id="ad686-214">(DIMENSIONS-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="ad686-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="ad686-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="ad686-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="ad686-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-217">CUBE_NAME</span></span><br />
<span data-ttu-id="ad686-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="ad686-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-221">27</span><span class="sxs-lookup"><span data-stu-id="ad686-221">27</span></span></p></td>
<td><p><span data-ttu-id="ad686-222">Gibt die Fremdschlüsselspalten zurück, die im Katalog von einem bestimmten Benutzer definiert wurden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="ad686-223">(FOREIGN_KEYS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="ad686-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-231">34</span><span class="sxs-lookup"><span data-stu-id="ad686-231">34</span></span></p></td>
<td><p><span data-ttu-id="ad686-232">Gibt Informationen zu den in einer Dimension unterstützten Hierarchien zurück.
</span><span class="sxs-lookup"><span data-stu-id="ad686-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="ad686-233">(HIERARCHIES-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="ad686-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="ad686-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="ad686-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="ad686-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-236">CUBE_NAME</span></span><br />
<span data-ttu-id="ad686-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="ad686-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-240"><strong>"adSchemaIndexes"</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-241">12</span><span class="sxs-lookup"><span data-stu-id="ad686-241">12</span></span></p></td>
<td><p><span data-ttu-id="ad686-242">Gibt die im Katalog definierten Indizes zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="ad686-243">(INDEXES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-246">INDEX_NAME</span></span><br />
<span data-ttu-id="ad686-247">TYP</span><span class="sxs-lookup"><span data-stu-id="ad686-247">TYPE</span></span><br />
<span data-ttu-id="ad686-248">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-250">8</span><span class="sxs-lookup"><span data-stu-id="ad686-250">8</span></span></p></td>
<td><p><span data-ttu-id="ad686-251">Gibt die im Katalog definierten Spalten zurück, die von einem bestimmten Benutzer als Schlüssel eingeschränkt werden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="ad686-252">(KEY_COLUMN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="ad686-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="ad686-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="ad686-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-258">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-258">TABLE_NAME</span></span><br />
<span data-ttu-id="ad686-259">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-261">35</span><span class="sxs-lookup"><span data-stu-id="ad686-261">35</span></span></p></td>
<td><p><span data-ttu-id="ad686-262">Gibt Informationen zu den in einer Dimension verfügbaren Ebenen zurück.
</span><span class="sxs-lookup"><span data-stu-id="ad686-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="ad686-263">(LEVELS-Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="ad686-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="ad686-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="ad686-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="ad686-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-266">CUBE_NAME</span></span><br />
<span data-ttu-id="ad686-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="ad686-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-272">36</span><span class="sxs-lookup"><span data-stu-id="ad686-272">36</span></span></p></td>
<td><p><span data-ttu-id="ad686-273">Gibt Informationen zu den verfügbaren Measures zurück.
</span><span class="sxs-lookup"><span data-stu-id="ad686-273">Returns information about the available measures.</span></span> <span data-ttu-id="ad686-274">(MEASURES-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="ad686-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="ad686-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="ad686-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="ad686-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-277">CUBE_NAME</span></span><br />
<span data-ttu-id="ad686-278">MESSGRÖßENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="ad686-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-281">38</span><span class="sxs-lookup"><span data-stu-id="ad686-281">38</span></span></p></td>
<td><p><span data-ttu-id="ad686-282">Gibt Informationen zu den verfügbaren Elementen zurück.
</span><span class="sxs-lookup"><span data-stu-id="ad686-282">Returns information about the available members.</span></span> <span data-ttu-id="ad686-283">(MEMBERS-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="ad686-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="ad686-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="ad686-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="ad686-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-286">CUBE_NAME</span></span><br />
<span data-ttu-id="ad686-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="ad686-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="ad686-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="ad686-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-293">MEMBER_CAPTION.</span><span class="sxs-lookup"><span data-stu-id="ad686-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="ad686-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="ad686-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="ad686-295">Tree-Operator (Weitere Informationen finden Sie in der OLE DB für OLAP-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="ad686-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-296"><strong>"adSchemaPrimaryKeys"</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-297">28</span><span class="sxs-lookup"><span data-stu-id="ad686-297">28</span></span></p></td>
<td><p><span data-ttu-id="ad686-298">Gibt die Primärschlüsselspalten zurück, die im Katalog von einem bestimmten Benutzer definiert wurden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="ad686-299">(PRIMARY_KEYS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-304">29</span><span class="sxs-lookup"><span data-stu-id="ad686-304">29</span></span></p></td>
<td><p><span data-ttu-id="ad686-305">Gibt Informationen zu den Spalten von Rowsets zurück, die von Prozeduren zurückgegeben werden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="ad686-306">(PROCEDURE_COLUMNS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="ad686-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="ad686-310">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-312">26</span><span class="sxs-lookup"><span data-stu-id="ad686-312">26</span></span></p></td>
<td><p><span data-ttu-id="ad686-313">Gibt Informationen zu den Parametern und Rückgabecodes der Prozeduren zurück.
</span><span class="sxs-lookup"><span data-stu-id="ad686-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="ad686-314">(PROCEDURE_PARAMETERS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="ad686-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="ad686-318">PARAMETERNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-320">16</span><span class="sxs-lookup"><span data-stu-id="ad686-320">16</span></span></p></td>
<td><p><span data-ttu-id="ad686-321">Gibt die im Katalog definierten Prozeduren zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="ad686-322">(PROCEDURES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="ad686-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="ad686-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ad686-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-328">37</span><span class="sxs-lookup"><span data-stu-id="ad686-328">37</span></span></p></td>
<td><p><span data-ttu-id="ad686-329">Gibt Informationen zu den verfügbaren Eigenschaften für jede Ebene der Dimension zurück.
</span><span class="sxs-lookup"><span data-stu-id="ad686-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="ad686-330">(PROPERTIES-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="ad686-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="ad686-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="ad686-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="ad686-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-333">CUBE_NAME</span></span><br />
<span data-ttu-id="ad686-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="ad686-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="ad686-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="ad686-339">EIGENSCHAFTSNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-341">-1</span><span class="sxs-lookup"><span data-stu-id="ad686-341">-1</span></span></p></td>
<td><p><span data-ttu-id="ad686-342">Wird verwendet, wenn der Anbieter eigene, nicht standardmäßige Schemaabfragen definiert.</span><span class="sxs-lookup"><span data-stu-id="ad686-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="ad686-343">&lt;Bestimmte Anbieter&gt;</span><span class="sxs-lookup"><span data-stu-id="ad686-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-345">22</span><span class="sxs-lookup"><span data-stu-id="ad686-345">22</span></span></p></td>
<td><p><span data-ttu-id="ad686-346">Gibt die (Basis-)Datentypen zurück, die vom Datenprovider unterstützt werden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="ad686-347">(PROVIDER_TYPES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-348">DATENTYP</span><span class="sxs-lookup"><span data-stu-id="ad686-348">DATA_TYPE</span></span><br />
<span data-ttu-id="ad686-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="ad686-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-351">9</span><span class="sxs-lookup"><span data-stu-id="ad686-351">9</span></span></p></td>
<td><p><span data-ttu-id="ad686-352">Gibt die im Katalog definierten referenziellen Einschränkungen zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="ad686-353">(REFERENTIAL_CONSTRAINTS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="ad686-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="ad686-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-358">17</span><span class="sxs-lookup"><span data-stu-id="ad686-358">17</span></span></p></td>
<td><p><span data-ttu-id="ad686-359">Gibt die Schemas (Datenbankobjekte) zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="ad686-360">(SCHEMATA-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="ad686-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="ad686-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="ad686-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-365">18</span><span class="sxs-lookup"><span data-stu-id="ad686-365">18</span></span></p></td>
<td><p><span data-ttu-id="ad686-366">Gibt die Konformitätsebenen, die Optionen und die Dialekte zurück, die von den Verarbeitungsdaten der SQL-Implementierung unterstützt werden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="ad686-367">(SQL_LANGUAGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-368">&lt;None&gt;</span><span class="sxs-lookup"><span data-stu-id="ad686-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-370">19</span><span class="sxs-lookup"><span data-stu-id="ad686-370">19</span></span></p></td>
<td><p><span data-ttu-id="ad686-371">Gibt die im Katalog definierten Statistiken zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="ad686-372">(STATISTICS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-375">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-377">10</span><span class="sxs-lookup"><span data-stu-id="ad686-377">10</span></span></p></td>
<td><p><span data-ttu-id="ad686-378">Gibt die im Katalog definierten Tabelleneinschränkungen zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="ad686-379">(TABLE_CONSTRAINTS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="ad686-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="ad686-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="ad686-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-385">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-385">TABLE_NAME</span></span><br />
<span data-ttu-id="ad686-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="ad686-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-388">14</span><span class="sxs-lookup"><span data-stu-id="ad686-388">14</span></span></p></td>
<td><p><span data-ttu-id="ad686-389">Gibt die im Katalog definierten Tabellenberechtigungen zurück, die einem bestimmten Benutzer zur Verfügung stehen oder von diesem erteilt werden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="ad686-390">(TABLE_PRIVILEGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-393">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-393">TABLE_NAME</span></span><br />
<span data-ttu-id="ad686-394">RECHTEFÜR</span><span class="sxs-lookup"><span data-stu-id="ad686-394">GRANTOR</span></span><br />
<span data-ttu-id="ad686-395">BERECHTIGTE</span><span class="sxs-lookup"><span data-stu-id="ad686-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-397">20</span><span class="sxs-lookup"><span data-stu-id="ad686-397">20</span></span></p></td>
<td><p><span data-ttu-id="ad686-398">Gibt die im Katalog definierten Tabellen (einschließlich Sichten) zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="ad686-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="ad686-399">(TABLES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-402">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-402">TABLE_NAME</span></span><br />
<span data-ttu-id="ad686-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ad686-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-405">21</span><span class="sxs-lookup"><span data-stu-id="ad686-405">21</span></span></p></td>
<td><p><span data-ttu-id="ad686-406">Gibt die im Katalog definierten Zeichenumwandlungen zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="ad686-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="ad686-407">(TRANSLATIONS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="ad686-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="ad686-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="ad686-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-412">39</span><span class="sxs-lookup"><span data-stu-id="ad686-412">39</span></span></p></td>
<td><p><span data-ttu-id="ad686-413">Reserviert für eine zukünftige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="ad686-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-415">15</span><span class="sxs-lookup"><span data-stu-id="ad686-415">15</span></span></p></td>
<td><p><span data-ttu-id="ad686-416">Gibt die im Katalog definierten USAGE-Berechtigungen zurück, die einem bestimmten Benutzer zur Verfügung stehen oder von diesem erteilt werden.
</span><span class="sxs-lookup"><span data-stu-id="ad686-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="ad686-417">(USAGE_PRIVILEGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="ad686-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="ad686-420">OBJEKTNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="ad686-421">OBJEKTTYP</span><span class="sxs-lookup"><span data-stu-id="ad686-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="ad686-422">RECHTEFÜR</span><span class="sxs-lookup"><span data-stu-id="ad686-422">GRANTOR</span></span><br />
<span data-ttu-id="ad686-423">BERECHTIGTE</span><span class="sxs-lookup"><span data-stu-id="ad686-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-425">24</span><span class="sxs-lookup"><span data-stu-id="ad686-425">24</span></span></p></td>
<td><p><span data-ttu-id="ad686-426">Gibt die Spalten zurück, von denen die angezeigten Tabellen abhängig sind, die im Katalog definiert sind und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="ad686-427">(VIEW_COLUMN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="ad686-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="ad686-430">ANSICHTSNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-432">23</span><span class="sxs-lookup"><span data-stu-id="ad686-432">23</span></span></p></td>
<td><p><span data-ttu-id="ad686-433">Gibt die im Katalog definierten Sichten zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="ad686-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="ad686-434">(VIEWS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="ad686-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="ad686-437">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="ad686-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="ad686-439">25</span><span class="sxs-lookup"><span data-stu-id="ad686-439">25</span></span></p></td>
<td><p><span data-ttu-id="ad686-440">Gibt die Tabellen zurück, von denen die angezeigten Tabellen abhängig sind, die im Katalog definiert sind und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="ad686-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="ad686-441">(VIEW_TABLE_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="ad686-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="ad686-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ad686-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="ad686-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ad686-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="ad686-444">ANSICHTSNAME</span><span class="sxs-lookup"><span data-stu-id="ad686-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ad686-445">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="ad686-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="ad686-446">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ad686-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad686-447">Konstante</span><span class="sxs-lookup"><span data-stu-id="ad686-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad686-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="ad686-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="ad686-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="ad686-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="ad686-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="ad686-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="ad686-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="ad686-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="ad686-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="ad686-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="ad686-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="ad686-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="ad686-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="ad686-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="ad686-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="ad686-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="ad686-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="ad686-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="ad686-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="ad686-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="ad686-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="ad686-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="ad686-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="ad686-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad686-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="ad686-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ad686-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="ad686-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="ad686-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="ad686-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="ad686-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="ad686-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="ad686-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="ad686-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="ad686-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="ad686-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="ad686-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="ad686-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="ad686-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="ad686-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad686-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="ad686-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad686-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="ad686-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

