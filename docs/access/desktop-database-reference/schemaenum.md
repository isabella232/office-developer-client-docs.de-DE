---
title: SchemaEnum (Access Desktop Database Reference)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308863"
---
# <a name="schemaenum"></a><span data-ttu-id="4b56e-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="4b56e-102">SchemaEnum</span></span>

<span data-ttu-id="4b56e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b56e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b56e-104">Der Typ des **Recordset** -Schemaobjekts wird angegeben, das von der [OpenSchema](openschema-method-ado.md)-Methode abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4b56e-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b56e-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b56e-105">Remarks</span></span>

<span data-ttu-id="4b56e-106">Weitere Informationen zu der Funktion und den Spalten, die für jede ADO-Konstante zurückgegeben werden, finden Sie in den Themen von Anhang B der *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="4b56e-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="4b56e-107">Die Namen der einzelnen Themen werden in Klammern im Abschnitt Description der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b56e-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="4b56e-108">Weitere Informationen zu der Funktion und den Spalten, die für jede ADO MD-Konstante zurückgegeben werden, finden Sie in Kapitel 23 der Dokumentation zu *OLE DB für OLAP*.</span><span class="sxs-lookup"><span data-stu-id="4b56e-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="4b56e-109">Die Namen der einzelnen Themen werden in Klammern aufgelistet und mit einem Sternchen (\*) in der Spalte Description der folgenden Tabelle gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="4b56e-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="4b56e-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span><span class="sxs-lookup"><span data-stu-id="4b56e-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="4b56e-111">Ein OLE DB-Datentyp von **\_DbType WSTR** entspricht beispielsweise einem ADO-Datentyp von **adWChar**.</span><span class="sxs-lookup"><span data-stu-id="4b56e-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="4b56e-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="4b56e-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="4b56e-113">ADO erstellt ein **Recordset**-Objekt und füllt dann jede Zeile mit den Werten, die von den **IDBInfo:: GetKeywords** -und **IDBInfo:: GetLiteralInfo** -Methoden zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="4b56e-114">Weitere Informationen zu diesen Methoden finden Sie im Abschnitt IDBInfo der *OLE DB Programmer es Reference*.</span><span class="sxs-lookup"><span data-stu-id="4b56e-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="4b56e-115">Konstante</span><span class="sxs-lookup"><span data-stu-id="4b56e-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="4b56e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4b56e-116">Value</span></span></p></th>
<th><p><span data-ttu-id="4b56e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b56e-117">Description</span></span></p></th>
<th><p><span data-ttu-id="4b56e-118">Einschränkungsspalten</span><span class="sxs-lookup"><span data-stu-id="4b56e-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-120">0</span><span class="sxs-lookup"><span data-stu-id="4b56e-120">0</span></span></p></td>
<td><p><span data-ttu-id="4b56e-121">Gibt die im Katalog definierten Assertionen zurück, die einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4b56e-122">(ASSERTIONS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4b56e-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-127">1</span><span class="sxs-lookup"><span data-stu-id="4b56e-127">1</span></span></p></td>
<td><p><span data-ttu-id="4b56e-128">Gibt die physikalischen Attribute zurück, die Katalogen zugeordnet sind, auf die vom DBMS zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4b56e-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="4b56e-129">(CATALOGS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-132">2</span><span class="sxs-lookup"><span data-stu-id="4b56e-132">2</span></span></p></td>
<td><p><span data-ttu-id="4b56e-133">Gibt die im Katalog definierten Zeichensätze zurück, auf die ein bestimmter Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4b56e-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4b56e-134">(CHARACTER_SETS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="4b56e-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-139">5</span><span class="sxs-lookup"><span data-stu-id="4b56e-139">5</span></span></p></td>
<td><p><span data-ttu-id="4b56e-140">Gibt die im Katalog definierten CHECK-Einschränkungen zurück, die einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4b56e-141">(CHECK_CONSTRAINTS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4b56e-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-146">3</span><span class="sxs-lookup"><span data-stu-id="4b56e-146">3</span></span></p></td>
<td><p><span data-ttu-id="4b56e-147">Gibt die im Katalog definierten Sortierungen zurück, auf die ein bestimmter Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4b56e-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4b56e-148">(COLLATIONS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="4b56e-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-153">13</span><span class="sxs-lookup"><span data-stu-id="4b56e-153">13</span></span></p></td>
<td><p><span data-ttu-id="4b56e-154">Gibt die im Katalog definierten Tabellenspaltenberechtigungen zurück, die einem bestimmten Benutzer zur Verfügung stehen oder von diesem erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="4b56e-155">(COLUMN_PRIVILEGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-158">TABLE_NAME</span></span><br />
<span data-ttu-id="4b56e-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="4b56e-160">RECHTEFÜR</span><span class="sxs-lookup"><span data-stu-id="4b56e-160">GRANTOR</span></span><br />
<span data-ttu-id="4b56e-161">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="4b56e-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-163">4</span><span class="sxs-lookup"><span data-stu-id="4b56e-163">4</span></span></p></td>
<td><p><span data-ttu-id="4b56e-164">Gibt die im Katalog definierten Tabellenspalten (einschließlich Sichten) zurück, auf die ein bestimmter Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4b56e-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4b56e-165">(COLUMNS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-168">TABLE_NAME</span></span><br />
<span data-ttu-id="4b56e-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-171">11</span><span class="sxs-lookup"><span data-stu-id="4b56e-171">11</span></span></p></td>
<td><p><span data-ttu-id="4b56e-172">Gibt die im Katalog definierten Spalten zurück, die von einer im Katalog definierten Domäne abhängig sind und einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="4b56e-173">(COLUMN_DOMAIN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="4b56e-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-176">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="4b56e-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-179">6</span><span class="sxs-lookup"><span data-stu-id="4b56e-179">6</span></span></p></td>
<td><p><span data-ttu-id="4b56e-180">Gibt die im Katalog definierten Spalten zurück, die von referenziellen Einschränkungen, eindeutigen Einschränkungen, CHECK-Einschränkungen und Assertionen verwendet werden und einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="4b56e-181">(CONSTRAINT_COLUMN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-184">TABLE_NAME</span></span><br />
<span data-ttu-id="4b56e-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-187">7</span><span class="sxs-lookup"><span data-stu-id="4b56e-187">7</span></span></p></td>
<td><p><span data-ttu-id="4b56e-188">Gibt die im Katalog definierten Tabellen zurück, die von referenziellen Einschränkungen, eindeutigen Einschränkungen, CHECK-Einschränkungen und Assertionen verwendet werden und einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="4b56e-189">(CONSTRAINT_TABLE_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-194">32</span><span class="sxs-lookup"><span data-stu-id="4b56e-194">32</span></span></p></td>
<td><p><span data-ttu-id="4b56e-195">Gibt Informationen zu den verfügbaren Cubes in einem Schema zurück (oder im Katalog, wenn der Anbieter keine Schemas unterstützt).</span><span class="sxs-lookup"><span data-stu-id="4b56e-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="4b56e-196">(CUBES-Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="4b56e-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="4b56e-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4b56e-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-201">30</span><span class="sxs-lookup"><span data-stu-id="4b56e-201">30</span></span></p></td>
<td><p><span data-ttu-id="4b56e-202">Gibt eine Liste anbieterspezifischer Schlüsselwörter zurück.</span><span class="sxs-lookup"><span data-stu-id="4b56e-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="4b56e-203">(IDBInfo:: getKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="4b56e-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-204">&lt;Keine&gt;</span><span class="sxs-lookup"><span data-stu-id="4b56e-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-206">31</span><span class="sxs-lookup"><span data-stu-id="4b56e-206">31</span></span></p></td>
<td><p><span data-ttu-id="4b56e-207">Gibt eine Liste anbieterspezifischer Literale zurück, die in Textbefehlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="4b56e-208">(IDBInfo:: GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="4b56e-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-209">&lt;Keine&gt;</span><span class="sxs-lookup"><span data-stu-id="4b56e-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-211">33</span><span class="sxs-lookup"><span data-stu-id="4b56e-211">33</span></span></p></td>
<td><p><span data-ttu-id="4b56e-212">Gibt Informationen zu den Dimensionen in einem bestimmten Cube zurück.</span><span class="sxs-lookup"><span data-stu-id="4b56e-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="4b56e-213">Es verfügt über eine Zeile für jede Dimension.</span><span class="sxs-lookup"><span data-stu-id="4b56e-213">It has one row for each dimension.</span></span> <span data-ttu-id="4b56e-214">(DIMENSIONS-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4b56e-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="4b56e-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4b56e-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-217">CUBE_NAME</span></span><br />
<span data-ttu-id="4b56e-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="4b56e-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-221">27</span><span class="sxs-lookup"><span data-stu-id="4b56e-221">27</span></span></p></td>
<td><p><span data-ttu-id="4b56e-222">Gibt die Fremdschlüsselspalten zurück, die im Katalog von einem bestimmten Benutzer definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="4b56e-223">(FOREIGN_KEYS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="4b56e-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-231">34</span><span class="sxs-lookup"><span data-stu-id="4b56e-231">34</span></span></p></td>
<td><p><span data-ttu-id="4b56e-232">Gibt Informationen zu den in einer Dimension unterstützten Hierarchien zurück.</span><span class="sxs-lookup"><span data-stu-id="4b56e-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="4b56e-233">(HIERARCHIES-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4b56e-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="4b56e-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4b56e-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-236">CUBE_NAME</span></span><br />
<span data-ttu-id="4b56e-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="4b56e-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-241">12</span><span class="sxs-lookup"><span data-stu-id="4b56e-241">12</span></span></p></td>
<td><p><span data-ttu-id="4b56e-242">Gibt die im Katalog definierten Indizes zurück, die einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4b56e-243">(INDEXES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-246">INDEX_NAME</span></span><br />
<span data-ttu-id="4b56e-247">Typ</span><span class="sxs-lookup"><span data-stu-id="4b56e-247">TYPE</span></span><br />
<span data-ttu-id="4b56e-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-250">8</span><span class="sxs-lookup"><span data-stu-id="4b56e-250">8</span></span></p></td>
<td><p><span data-ttu-id="4b56e-251">Gibt die im Katalog definierten Spalten zurück, die von einem bestimmten Benutzer als Schlüssel eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="4b56e-252">(KEY_COLUMN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4b56e-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="4b56e-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-258">TABLE_NAME</span></span><br />
<span data-ttu-id="4b56e-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-261">35</span><span class="sxs-lookup"><span data-stu-id="4b56e-261">35</span></span></p></td>
<td><p><span data-ttu-id="4b56e-262">Gibt Informationen zu den in einer Dimension verfügbaren Ebenen zurück.</span><span class="sxs-lookup"><span data-stu-id="4b56e-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="4b56e-263">(LEVELS-Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="4b56e-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="4b56e-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4b56e-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-266">CUBE_NAME</span></span><br />
<span data-ttu-id="4b56e-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="4b56e-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-272">36</span><span class="sxs-lookup"><span data-stu-id="4b56e-272">36</span></span></p></td>
<td><p><span data-ttu-id="4b56e-273">Gibt Informationen zu den verfügbaren Measures zurück.</span><span class="sxs-lookup"><span data-stu-id="4b56e-273">Returns information about the available measures.</span></span> <span data-ttu-id="4b56e-274">(MEASURES-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4b56e-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="4b56e-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4b56e-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-277">CUBE_NAME</span></span><br />
<span data-ttu-id="4b56e-278">MESSGRÖßE</span><span class="sxs-lookup"><span data-stu-id="4b56e-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="4b56e-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-281">38</span><span class="sxs-lookup"><span data-stu-id="4b56e-281">38</span></span></p></td>
<td><p><span data-ttu-id="4b56e-282">Gibt Informationen zu den verfügbaren Elementen zurück.</span><span class="sxs-lookup"><span data-stu-id="4b56e-282">Returns information about the available members.</span></span> <span data-ttu-id="4b56e-283">(MEMBERS-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4b56e-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="4b56e-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4b56e-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-286">CUBE_NAME</span></span><br />
<span data-ttu-id="4b56e-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="4b56e-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="4b56e-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="4b56e-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="4b56e-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="4b56e-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="4b56e-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="4b56e-295">Tree-Operator (Weitere Informationen finden Sie in der Dokumentation zu OLE DB für OLAP.)</span><span class="sxs-lookup"><span data-stu-id="4b56e-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-297">28</span><span class="sxs-lookup"><span data-stu-id="4b56e-297">28</span></span></p></td>
<td><p><span data-ttu-id="4b56e-298">Gibt die Primärschlüsselspalten zurück, die im Katalog von einem bestimmten Benutzer definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="4b56e-299">(PRIMARY_KEYS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-304">29</span><span class="sxs-lookup"><span data-stu-id="4b56e-304">29</span></span></p></td>
<td><p><span data-ttu-id="4b56e-305">Gibt Informationen zu den Spalten von Rowsets zurück, die von Prozeduren zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="4b56e-306">(PROCEDURE_COLUMNS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="4b56e-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-312">26</span><span class="sxs-lookup"><span data-stu-id="4b56e-312">26</span></span></p></td>
<td><p><span data-ttu-id="4b56e-313">Gibt Informationen zu den Parametern und Rückgabecodes der Prozeduren zurück.</span><span class="sxs-lookup"><span data-stu-id="4b56e-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="4b56e-314">(PROCEDURE_PARAMETERS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="4b56e-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-320">16</span><span class="sxs-lookup"><span data-stu-id="4b56e-320">16</span></span></p></td>
<td><p><span data-ttu-id="4b56e-321">Gibt die im Katalog definierten Prozeduren zurück, die einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4b56e-322">(PROCEDURES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="4b56e-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="4b56e-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-328">37</span><span class="sxs-lookup"><span data-stu-id="4b56e-328">37</span></span></p></td>
<td><p><span data-ttu-id="4b56e-329">Gibt Informationen zu den verfügbaren Eigenschaften für jede Ebene der Dimension zurück.</span><span class="sxs-lookup"><span data-stu-id="4b56e-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="4b56e-330">(PROPERTIES-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4b56e-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="4b56e-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4b56e-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-333">CUBE_NAME</span></span><br />
<span data-ttu-id="4b56e-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4b56e-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="4b56e-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="4b56e-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-341">-1</span><span class="sxs-lookup"><span data-stu-id="4b56e-341">-1</span></span></p></td>
<td><p><span data-ttu-id="4b56e-342">Wird verwendet, wenn der Anbieter eigene, nicht standardmäßige Schemaabfragen definiert.</span><span class="sxs-lookup"><span data-stu-id="4b56e-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="4b56e-343">&lt;Anbieter spezifisch&gt;</span><span class="sxs-lookup"><span data-stu-id="4b56e-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-345">22</span><span class="sxs-lookup"><span data-stu-id="4b56e-345">22</span></span></p></td>
<td><p><span data-ttu-id="4b56e-346">Gibt die (Basis-)Datentypen zurück, die vom Datenprovider unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="4b56e-347">(PROVIDER_TYPES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4b56e-348">DATA_TYPE</span></span><br />
<span data-ttu-id="4b56e-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="4b56e-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-351">9</span><span class="sxs-lookup"><span data-stu-id="4b56e-351">9</span></span></p></td>
<td><p><span data-ttu-id="4b56e-352">Gibt die im Katalog definierten referenziellen Einschränkungen zurück, die einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4b56e-353">(REFERENTIAL_CONSTRAINTS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4b56e-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-358">17</span><span class="sxs-lookup"><span data-stu-id="4b56e-358">17</span></span></p></td>
<td><p><span data-ttu-id="4b56e-359">Gibt die Schemas (Datenbankobjekte) zurück, die einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="4b56e-360">(SCHEMATA-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="4b56e-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4b56e-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="4b56e-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-365">18</span><span class="sxs-lookup"><span data-stu-id="4b56e-365">18</span></span></p></td>
<td><p><span data-ttu-id="4b56e-366">Gibt die Konformitätsebenen, die Optionen und die Dialekte zurück, die von den Verarbeitungsdaten der SQL-Implementierung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="4b56e-367">(SQL_LANGUAGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-368">&lt;Keine&gt;</span><span class="sxs-lookup"><span data-stu-id="4b56e-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-370">19</span><span class="sxs-lookup"><span data-stu-id="4b56e-370">19</span></span></p></td>
<td><p><span data-ttu-id="4b56e-371">Gibt die im Katalog definierten Statistiken zurück, die einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4b56e-372">(STATISTICS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-377">10</span><span class="sxs-lookup"><span data-stu-id="4b56e-377">10</span></span></p></td>
<td><p><span data-ttu-id="4b56e-378">Gibt die im Katalog definierten Tabelleneinschränkungen zurück, die einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4b56e-379">(TABLE_CONSTRAINTS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4b56e-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="4b56e-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-385">TABLE_NAME</span></span><br />
<span data-ttu-id="4b56e-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="4b56e-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-388">14</span><span class="sxs-lookup"><span data-stu-id="4b56e-388">14</span></span></p></td>
<td><p><span data-ttu-id="4b56e-389">Gibt die im Katalog definierten Tabellenberechtigungen zurück, die einem bestimmten Benutzer zur Verfügung stehen oder von diesem erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="4b56e-390">(TABLE_PRIVILEGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-393">TABLE_NAME</span></span><br />
<span data-ttu-id="4b56e-394">RECHTEFÜR</span><span class="sxs-lookup"><span data-stu-id="4b56e-394">GRANTOR</span></span><br />
<span data-ttu-id="4b56e-395">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="4b56e-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-397">20</span><span class="sxs-lookup"><span data-stu-id="4b56e-397">20</span></span></p></td>
<td><p><span data-ttu-id="4b56e-398">Gibt die im Katalog definierten Tabellen (einschließlich Sichten) zurück, auf die ein bestimmter Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4b56e-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4b56e-399">(TABLES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-402">TABLE_NAME</span></span><br />
<span data-ttu-id="4b56e-403">_TYPE</span><span class="sxs-lookup"><span data-stu-id="4b56e-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-405">21</span><span class="sxs-lookup"><span data-stu-id="4b56e-405">21</span></span></p></td>
<td><p><span data-ttu-id="4b56e-406">Gibt die im Katalog definierten Zeichenumwandlungen zurück, auf die ein bestimmter Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4b56e-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4b56e-407">(TRANSLATIONS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="4b56e-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-412">39</span><span class="sxs-lookup"><span data-stu-id="4b56e-412">39</span></span></p></td>
<td><p><span data-ttu-id="4b56e-413">Reserviert für eine zukünftige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="4b56e-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-415">15</span><span class="sxs-lookup"><span data-stu-id="4b56e-415">15</span></span></p></td>
<td><p><span data-ttu-id="4b56e-416">Gibt die im Katalog definierten USAGE-Berechtigungen zurück, die einem bestimmten Benutzer zur Verfügung stehen oder von diesem erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="4b56e-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="4b56e-417">(USAGE_PRIVILEGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="4b56e-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="4b56e-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="4b56e-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="4b56e-422">RECHTEFÜR</span><span class="sxs-lookup"><span data-stu-id="4b56e-422">GRANTOR</span></span><br />
<span data-ttu-id="4b56e-423">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="4b56e-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-425">24</span><span class="sxs-lookup"><span data-stu-id="4b56e-425">24</span></span></p></td>
<td><p><span data-ttu-id="4b56e-426">Gibt die Spalten zurück, von denen die angezeigten Tabellen abhängig sind, die im Katalog definiert sind und einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="4b56e-427">(VIEW_COLUMN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="4b56e-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-432">23</span><span class="sxs-lookup"><span data-stu-id="4b56e-432">23</span></span></p></td>
<td><p><span data-ttu-id="4b56e-433">Gibt die im Katalog definierten Sichten zurück, auf die ein bestimmter Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4b56e-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4b56e-434">(VIEWS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4b56e-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4b56e-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4b56e-439">25</span><span class="sxs-lookup"><span data-stu-id="4b56e-439">25</span></span></p></td>
<td><p><span data-ttu-id="4b56e-440">Gibt die Tabellen zurück, von denen die angezeigten Tabellen abhängig sind, die im Katalog definiert sind und einem bestimmten Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="4b56e-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="4b56e-441">(VIEW_TABLE_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="4b56e-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4b56e-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4b56e-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="4b56e-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4b56e-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="4b56e-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="4b56e-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4b56e-445">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="4b56e-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="4b56e-446">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="4b56e-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b56e-447">Konstante</span><span class="sxs-lookup"><span data-stu-id="4b56e-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-448">AdoEnums. Schema. ASSERTs</span><span class="sxs-lookup"><span data-stu-id="4b56e-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-449">AdoEnums. Schema. CATALOGs</span><span class="sxs-lookup"><span data-stu-id="4b56e-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-450">AdoEnums. Schema. CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="4b56e-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-451">AdoEnums. Schema. CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="4b56e-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-452">AdoEnums. Schema. COLLation</span><span class="sxs-lookup"><span data-stu-id="4b56e-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-453">AdoEnums. Schema. COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="4b56e-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-454">AdoEnums. Schema. COLUMNS</span><span class="sxs-lookup"><span data-stu-id="4b56e-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-455">AdoEnums. Schema. COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="4b56e-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-456">AdoEnums. Schema. CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="4b56e-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-457">AdoEnums. Schema. CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="4b56e-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-458">AdoEnums. Schema. Cubes</span><span class="sxs-lookup"><span data-stu-id="4b56e-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-459">AdoEnums. Schema. DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="4b56e-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-460">AdoEnums. Schema. DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="4b56e-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-461">AdoEnums. Schema. DIMENSIONs</span><span class="sxs-lookup"><span data-stu-id="4b56e-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-462">AdoEnums. Schema. FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="4b56e-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-463">AdoEnums. Schema. HIERARCHIEs</span><span class="sxs-lookup"><span data-stu-id="4b56e-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-464">AdoEnums. Schema. INDEXes</span><span class="sxs-lookup"><span data-stu-id="4b56e-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-465">AdoEnums. Schema. KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="4b56e-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-466">AdoEnums. Schema. LEVELS</span><span class="sxs-lookup"><span data-stu-id="4b56e-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-467">AdoEnums. Schema. MEASUREs</span><span class="sxs-lookup"><span data-stu-id="4b56e-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-468">AdoEnums. Schema. MEMBERS</span><span class="sxs-lookup"><span data-stu-id="4b56e-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-469">AdoEnums. Schema. PRIMARy</span><span class="sxs-lookup"><span data-stu-id="4b56e-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-470">AdoEnums. Schema. PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="4b56e-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-471">AdoEnums. Schema. PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b56e-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-472">AdoEnums. Schema. PROCEDURes</span><span class="sxs-lookup"><span data-stu-id="4b56e-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-473">AdoEnums. Schema. PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4b56e-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-474">AdoEnums. Schema. PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="4b56e-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-475">AdoEnums. Schema. PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="4b56e-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-476">AdoEnums. Schema. REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="4b56e-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-477">AdoEnums. Schema. SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="4b56e-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-478">AdoEnums. Schema. sqlLANGUAGEs</span><span class="sxs-lookup"><span data-stu-id="4b56e-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-479">AdoEnums. Schema. STATISTICs</span><span class="sxs-lookup"><span data-stu-id="4b56e-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-480">AdoEnums. Schema. TableSchema</span><span class="sxs-lookup"><span data-stu-id="4b56e-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-481">AdoEnums. Schema. TableSchema-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="4b56e-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-482">AdoEnums. Schema. TABLEs</span><span class="sxs-lookup"><span data-stu-id="4b56e-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-483">AdoEnums. Schema. TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="4b56e-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-484">AdoEnums. Schema. TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="4b56e-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-485">AdoEnums. Schema. USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="4b56e-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-486">AdoEnums. Schema. VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="4b56e-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b56e-487">AdoEnums. Schema. VIEWS</span><span class="sxs-lookup"><span data-stu-id="4b56e-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b56e-488">AdoEnums. Schema. VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="4b56e-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

