---
title: SchemaEnum (Access PC-Datenbank-Referenz)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a6f1e174253904adf7392aa7ae19786103e55843
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863353"
---
# <a name="schemaenum"></a><span data-ttu-id="9f44b-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="9f44b-102">SchemaEnum</span></span>

<span data-ttu-id="9f44b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f44b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9f44b-104">Der Typ des **Recordset** -Schemaobjekts wird angegeben, das von der [OpenSchema](openschema-method-ado.md)-Methode abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9f44b-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f44b-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f44b-105">Remarks</span></span>

<span data-ttu-id="9f44b-106">Weitere Informationen über die Funktion und den Spalten, die für jede ADO-Konstante zurückgegeben finden Sie in den Themen von Anhang B der *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="9f44b-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="9f44b-107">Die Namen der einzelnen Themen wird in Klammern im Abschnitt Beschreibung in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f44b-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="9f44b-108">Weitere Informationen über die Funktion und den Spalten, die für jede ADO MD-Konstante zurückgegeben finden Sie in Kapitel 23 der Dokumentation zu *OLE DB für OLAP* .</span><span class="sxs-lookup"><span data-stu-id="9f44b-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="9f44b-109">Die Namen der einzelnen Themen, die in Klammern aufgelistet und mit einem Sternchen gekennzeichnet ist (\*) in der Spalte Beschreibung in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9f44b-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="9f44b-110">Übersetzen Sie die Datentypen der Spalten in der Dokumentation zu OLE DB in ADO-Datentypen anhand der Spalte Beschreibung des Themas ADO [DataTypeEnum-Wert](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="9f44b-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="9f44b-111">Angenommen, ein OLE DB-Datentyp des **DATENBANKTYP\_WSTR** ein ADO-Datentyp des **AdWChar**entspricht.</span><span class="sxs-lookup"><span data-stu-id="9f44b-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="9f44b-112">ADO generiert Schema-ähnliche Ergebnisse für die Konstanten, die **AdSchemaDBInfoKeywords** und **AdSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="9f44b-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="9f44b-113">ADO ein **Recordset-Objekt**erstellt, und füllt dann jede Zeile mit den Werten, die von den Methoden **IDBInfo:: GetKeywords** und **:: GetLiteralInfo** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f44b-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="9f44b-114">Weitere Informationen zu diesen Methoden finden Sie im Abschnitt "IDBInfo" der *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="9f44b-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="9f44b-115">Konstante</span><span class="sxs-lookup"><span data-stu-id="9f44b-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="9f44b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9f44b-116">Value</span></span></p></th>
<th><p><span data-ttu-id="9f44b-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f44b-117">Description</span></span></p></th>
<th><p><span data-ttu-id="9f44b-118">Einschränkungsspalten</span><span class="sxs-lookup"><span data-stu-id="9f44b-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-120">0</span><span class="sxs-lookup"><span data-stu-id="9f44b-120">0</span></span></p></td>
<td><p><span data-ttu-id="9f44b-121">Gibt die im Katalog definierten Assertionen zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9f44b-122">(ASSERTIONS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9f44b-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-127">1</span><span class="sxs-lookup"><span data-stu-id="9f44b-127">1</span></span></p></td>
<td><p><span data-ttu-id="9f44b-128">Gibt die physikalischen Attribute zurück, die Katalogen zugeordnet sind, auf die vom DBMS zugegriffen werden kann.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="9f44b-129">(CATALOGS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-132">2</span><span class="sxs-lookup"><span data-stu-id="9f44b-132">2</span></span></p></td>
<td><p><span data-ttu-id="9f44b-133">Gibt die im Katalog definierten Zeichensätze zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9f44b-134">(CHARACTER_SETS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="9f44b-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-139">5</span><span class="sxs-lookup"><span data-stu-id="9f44b-139">5</span></span></p></td>
<td><p><span data-ttu-id="9f44b-140">Gibt die im Katalog definierten CHECK-Einschränkungen zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9f44b-141">(CHECK_CONSTRAINTS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9f44b-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-146">3</span><span class="sxs-lookup"><span data-stu-id="9f44b-146">3</span></span></p></td>
<td><p><span data-ttu-id="9f44b-147">Gibt die im Katalog definierten Sortierungen zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9f44b-148">(COLLATIONS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="9f44b-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-153">13</span><span class="sxs-lookup"><span data-stu-id="9f44b-153">13</span></span></p></td>
<td><p><span data-ttu-id="9f44b-154">Gibt die im Katalog definierten Tabellenspaltenberechtigungen zurück, die einem bestimmten Benutzer zur Verfügung stehen oder von diesem erteilt werden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="9f44b-155">(COLUMN_PRIVILEGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-158">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-158">TABLE_NAME</span></span><br />
<span data-ttu-id="9f44b-159">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="9f44b-160">RECHTEFÜR</span><span class="sxs-lookup"><span data-stu-id="9f44b-160">GRANTOR</span></span><br />
<span data-ttu-id="9f44b-161">BERECHTIGTE</span><span class="sxs-lookup"><span data-stu-id="9f44b-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-162"><strong>"adSchemaColumns"</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-163">4</span><span class="sxs-lookup"><span data-stu-id="9f44b-163">4</span></span></p></td>
<td><p><span data-ttu-id="9f44b-164">Gibt die im Katalog definierten Tabellenspalten (einschließlich Sichten) zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9f44b-165">(COLUMNS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-168">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-168">TABLE_NAME</span></span><br />
<span data-ttu-id="9f44b-169">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-171">11</span><span class="sxs-lookup"><span data-stu-id="9f44b-171">11</span></span></p></td>
<td><p><span data-ttu-id="9f44b-172">Gibt die im Katalog definierten Spalten zurück, die von einer im Katalog definierten Domäne abhängig sind und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="9f44b-173">(COLUMN_DOMAIN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="9f44b-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-176">DOMÄNENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="9f44b-177">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-179">6</span><span class="sxs-lookup"><span data-stu-id="9f44b-179">6</span></span></p></td>
<td><p><span data-ttu-id="9f44b-180">Gibt die im Katalog definierten Spalten zurück, die von referenziellen Einschränkungen, eindeutigen Einschränkungen, CHECK-Einschränkungen und Assertionen verwendet werden und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="9f44b-181">(CONSTRAINT_COLUMN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-184">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-184">TABLE_NAME</span></span><br />
<span data-ttu-id="9f44b-185">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-187">7</span><span class="sxs-lookup"><span data-stu-id="9f44b-187">7</span></span></p></td>
<td><p><span data-ttu-id="9f44b-188">Gibt die im Katalog definierten Tabellen zurück, die von referenziellen Einschränkungen, eindeutigen Einschränkungen, CHECK-Einschränkungen und Assertionen verwendet werden und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="9f44b-189">(CONSTRAINT_TABLE_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-192">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-194">32</span><span class="sxs-lookup"><span data-stu-id="9f44b-194">32</span></span></p></td>
<td><p><span data-ttu-id="9f44b-195">Gibt Informationen zu den verfügbaren Cubes in einem Schema zurück (oder im Katalog, wenn der Anbieter keine Schemas unterstützt).
</span><span class="sxs-lookup"><span data-stu-id="9f44b-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="9f44b-196">(CUBES-Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="9f44b-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="9f44b-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9f44b-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-201">30</span><span class="sxs-lookup"><span data-stu-id="9f44b-201">30</span></span></p></td>
<td><p><span data-ttu-id="9f44b-202">Gibt eine Liste anbieterspezifischer Schlüsselwörter zurück.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="9f44b-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="9f44b-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-204">&lt;None&gt;</span><span class="sxs-lookup"><span data-stu-id="9f44b-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-206">31</span><span class="sxs-lookup"><span data-stu-id="9f44b-206">31</span></span></p></td>
<td><p><span data-ttu-id="9f44b-207">Gibt eine Liste anbieterspezifischer Literale zurück, die in Textbefehlen verwendet werden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="9f44b-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="9f44b-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-209">&lt;None&gt;</span><span class="sxs-lookup"><span data-stu-id="9f44b-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-211">33</span><span class="sxs-lookup"><span data-stu-id="9f44b-211">33</span></span></p></td>
<td><p><span data-ttu-id="9f44b-212">Gibt Informationen zu den Dimensionen in einem bestimmten Cube zurück.</span><span class="sxs-lookup"><span data-stu-id="9f44b-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="9f44b-213">Es wurde eine Zeile für jede Dimension.</span><span class="sxs-lookup"><span data-stu-id="9f44b-213">It has one row for each dimension.</span></span> <span data-ttu-id="9f44b-214">(DIMENSIONS-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9f44b-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="9f44b-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9f44b-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-217">CUBE_NAME</span></span><br />
<span data-ttu-id="9f44b-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="9f44b-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-221">27</span><span class="sxs-lookup"><span data-stu-id="9f44b-221">27</span></span></p></td>
<td><p><span data-ttu-id="9f44b-222">Gibt die Fremdschlüsselspalten zurück, die im Katalog von einem bestimmten Benutzer definiert wurden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="9f44b-223">(FOREIGN_KEYS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="9f44b-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-231">34</span><span class="sxs-lookup"><span data-stu-id="9f44b-231">34</span></span></p></td>
<td><p><span data-ttu-id="9f44b-232">Gibt Informationen zu den in einer Dimension unterstützten Hierarchien zurück.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="9f44b-233">(HIERARCHIES-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9f44b-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="9f44b-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9f44b-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-236">CUBE_NAME</span></span><br />
<span data-ttu-id="9f44b-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="9f44b-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-240"><strong>"adSchemaIndexes"</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-241">12</span><span class="sxs-lookup"><span data-stu-id="9f44b-241">12</span></span></p></td>
<td><p><span data-ttu-id="9f44b-242">Gibt die im Katalog definierten Indizes zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9f44b-243">(INDEXES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-246">INDEX_NAME</span></span><br />
<span data-ttu-id="9f44b-247">TYP</span><span class="sxs-lookup"><span data-stu-id="9f44b-247">TYPE</span></span><br />
<span data-ttu-id="9f44b-248">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-250">8</span><span class="sxs-lookup"><span data-stu-id="9f44b-250">8</span></span></p></td>
<td><p><span data-ttu-id="9f44b-251">Gibt die im Katalog definierten Spalten zurück, die von einem bestimmten Benutzer als Schlüssel eingeschränkt werden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="9f44b-252">(KEY_COLUMN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9f44b-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="9f44b-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-258">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-258">TABLE_NAME</span></span><br />
<span data-ttu-id="9f44b-259">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-261">35</span><span class="sxs-lookup"><span data-stu-id="9f44b-261">35</span></span></p></td>
<td><p><span data-ttu-id="9f44b-262">Gibt Informationen zu den in einer Dimension verfügbaren Ebenen zurück.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="9f44b-263">(LEVELS-Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="9f44b-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="9f44b-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9f44b-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-266">CUBE_NAME</span></span><br />
<span data-ttu-id="9f44b-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="9f44b-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-272">36</span><span class="sxs-lookup"><span data-stu-id="9f44b-272">36</span></span></p></td>
<td><p><span data-ttu-id="9f44b-273">Gibt Informationen zu den verfügbaren Measures zurück.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-273">Returns information about the available measures.</span></span> <span data-ttu-id="9f44b-274">(MEASURES-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9f44b-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="9f44b-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9f44b-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-277">CUBE_NAME</span></span><br />
<span data-ttu-id="9f44b-278">MESSGRÖßENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="9f44b-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-281">38</span><span class="sxs-lookup"><span data-stu-id="9f44b-281">38</span></span></p></td>
<td><p><span data-ttu-id="9f44b-282">Gibt Informationen zu den verfügbaren Elementen zurück.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-282">Returns information about the available members.</span></span> <span data-ttu-id="9f44b-283">(MEMBERS-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9f44b-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="9f44b-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9f44b-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-286">CUBE_NAME</span></span><br />
<span data-ttu-id="9f44b-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="9f44b-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="9f44b-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="9f44b-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-293">MEMBER_CAPTION.</span><span class="sxs-lookup"><span data-stu-id="9f44b-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="9f44b-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="9f44b-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="9f44b-295">Tree-Operator (Weitere Informationen finden Sie in der OLE DB für OLAP-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="9f44b-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-296"><strong>"adSchemaPrimaryKeys"</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-297">28</span><span class="sxs-lookup"><span data-stu-id="9f44b-297">28</span></span></p></td>
<td><p><span data-ttu-id="9f44b-298">Gibt die Primärschlüsselspalten zurück, die im Katalog von einem bestimmten Benutzer definiert wurden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="9f44b-299">(PRIMARY_KEYS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-304">29</span><span class="sxs-lookup"><span data-stu-id="9f44b-304">29</span></span></p></td>
<td><p><span data-ttu-id="9f44b-305">Gibt Informationen zu den Spalten von Rowsets zurück, die von Prozeduren zurückgegeben werden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="9f44b-306">(PROCEDURE_COLUMNS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="9f44b-310">SPALTENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-312">26</span><span class="sxs-lookup"><span data-stu-id="9f44b-312">26</span></span></p></td>
<td><p><span data-ttu-id="9f44b-313">Gibt Informationen zu den Parametern und Rückgabecodes der Prozeduren zurück.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="9f44b-314">(PROCEDURE_PARAMETERS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="9f44b-318">PARAMETERNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-320">16</span><span class="sxs-lookup"><span data-stu-id="9f44b-320">16</span></span></p></td>
<td><p><span data-ttu-id="9f44b-321">Gibt die im Katalog definierten Prozeduren zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9f44b-322">(PROCEDURES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="9f44b-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="9f44b-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-328">37</span><span class="sxs-lookup"><span data-stu-id="9f44b-328">37</span></span></p></td>
<td><p><span data-ttu-id="9f44b-329">Gibt Informationen zu den verfügbaren Eigenschaften für jede Ebene der Dimension zurück.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="9f44b-330">(PROPERTIES-Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9f44b-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="9f44b-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9f44b-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-333">CUBE_NAME</span></span><br />
<span data-ttu-id="9f44b-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9f44b-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="9f44b-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="9f44b-339">EIGENSCHAFTSNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-341">-1</span><span class="sxs-lookup"><span data-stu-id="9f44b-341">-1</span></span></p></td>
<td><p><span data-ttu-id="9f44b-342">Wird verwendet, wenn der Anbieter eigene, nicht standardmäßige Schemaabfragen definiert.</span><span class="sxs-lookup"><span data-stu-id="9f44b-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="9f44b-343">&lt;Bestimmte Anbieter&gt;</span><span class="sxs-lookup"><span data-stu-id="9f44b-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-345">22</span><span class="sxs-lookup"><span data-stu-id="9f44b-345">22</span></span></p></td>
<td><p><span data-ttu-id="9f44b-346">Gibt die (Basis-)Datentypen zurück, die vom Datenprovider unterstützt werden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="9f44b-347">(PROVIDER_TYPES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-348">DATENTYP</span><span class="sxs-lookup"><span data-stu-id="9f44b-348">DATA_TYPE</span></span><br />
<span data-ttu-id="9f44b-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="9f44b-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-351">9</span><span class="sxs-lookup"><span data-stu-id="9f44b-351">9</span></span></p></td>
<td><p><span data-ttu-id="9f44b-352">Gibt die im Katalog definierten referenziellen Einschränkungen zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9f44b-353">(REFERENTIAL_CONSTRAINTS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9f44b-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-358">17</span><span class="sxs-lookup"><span data-stu-id="9f44b-358">17</span></span></p></td>
<td><p><span data-ttu-id="9f44b-359">Gibt die Schemas (Datenbankobjekte) zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="9f44b-360">(SCHEMATA-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="9f44b-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9f44b-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="9f44b-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-365">18</span><span class="sxs-lookup"><span data-stu-id="9f44b-365">18</span></span></p></td>
<td><p><span data-ttu-id="9f44b-366">Gibt die Konformitätsebenen, die Optionen und die Dialekte zurück, die von den Verarbeitungsdaten der SQL-Implementierung unterstützt werden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="9f44b-367">(SQL_LANGUAGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-368">&lt;None&gt;</span><span class="sxs-lookup"><span data-stu-id="9f44b-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-370">19</span><span class="sxs-lookup"><span data-stu-id="9f44b-370">19</span></span></p></td>
<td><p><span data-ttu-id="9f44b-371">Gibt die im Katalog definierten Statistiken zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9f44b-372">(STATISTICS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-375">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-377">10</span><span class="sxs-lookup"><span data-stu-id="9f44b-377">10</span></span></p></td>
<td><p><span data-ttu-id="9f44b-378">Gibt die im Katalog definierten Tabelleneinschränkungen zurück, die einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9f44b-379">(TABLE_CONSTRAINTS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9f44b-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="9f44b-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-385">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-385">TABLE_NAME</span></span><br />
<span data-ttu-id="9f44b-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="9f44b-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-388">14</span><span class="sxs-lookup"><span data-stu-id="9f44b-388">14</span></span></p></td>
<td><p><span data-ttu-id="9f44b-389">Gibt die im Katalog definierten Tabellenberechtigungen zurück, die einem bestimmten Benutzer zur Verfügung stehen oder von diesem erteilt werden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="9f44b-390">(TABLE_PRIVILEGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-393">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-393">TABLE_NAME</span></span><br />
<span data-ttu-id="9f44b-394">RECHTEFÜR</span><span class="sxs-lookup"><span data-stu-id="9f44b-394">GRANTOR</span></span><br />
<span data-ttu-id="9f44b-395">BERECHTIGTE</span><span class="sxs-lookup"><span data-stu-id="9f44b-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-397">20</span><span class="sxs-lookup"><span data-stu-id="9f44b-397">20</span></span></p></td>
<td><p><span data-ttu-id="9f44b-398">Gibt die im Katalog definierten Tabellen (einschließlich Sichten) zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9f44b-399">(TABLES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-402">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-402">TABLE_NAME</span></span><br />
<span data-ttu-id="9f44b-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="9f44b-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-405">21</span><span class="sxs-lookup"><span data-stu-id="9f44b-405">21</span></span></p></td>
<td><p><span data-ttu-id="9f44b-406">Gibt die im Katalog definierten Zeichenumwandlungen zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9f44b-407">(TRANSLATIONS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="9f44b-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-412">39</span><span class="sxs-lookup"><span data-stu-id="9f44b-412">39</span></span></p></td>
<td><p><span data-ttu-id="9f44b-413">Reserviert für eine zukünftige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="9f44b-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-415">15</span><span class="sxs-lookup"><span data-stu-id="9f44b-415">15</span></span></p></td>
<td><p><span data-ttu-id="9f44b-416">Gibt die im Katalog definierten USAGE-Berechtigungen zurück, die einem bestimmten Benutzer zur Verfügung stehen oder von diesem erteilt werden.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="9f44b-417">(USAGE_PRIVILEGES-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="9f44b-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-420">OBJEKTNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="9f44b-421">OBJEKTTYP</span><span class="sxs-lookup"><span data-stu-id="9f44b-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="9f44b-422">RECHTEFÜR</span><span class="sxs-lookup"><span data-stu-id="9f44b-422">GRANTOR</span></span><br />
<span data-ttu-id="9f44b-423">BERECHTIGTE</span><span class="sxs-lookup"><span data-stu-id="9f44b-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-425">24</span><span class="sxs-lookup"><span data-stu-id="9f44b-425">24</span></span></p></td>
<td><p><span data-ttu-id="9f44b-426">Gibt die Spalten zurück, von denen die angezeigten Tabellen abhängig sind, die im Katalog definiert sind und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="9f44b-427">(VIEW_COLUMN_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="9f44b-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-430">ANSICHTSNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-432">23</span><span class="sxs-lookup"><span data-stu-id="9f44b-432">23</span></span></p></td>
<td><p><span data-ttu-id="9f44b-433">Gibt die im Katalog definierten Sichten zurück, auf die ein bestimmter Benutzer zugreifen kann.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9f44b-434">(VIEWS-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9f44b-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-437">TABELLENNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9f44b-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9f44b-439">25</span><span class="sxs-lookup"><span data-stu-id="9f44b-439">25</span></span></p></td>
<td><p><span data-ttu-id="9f44b-440">Gibt die Tabellen zurück, von denen die angezeigten Tabellen abhängig sind, die im Katalog definiert sind und einem bestimmten Benutzer gehören.
</span><span class="sxs-lookup"><span data-stu-id="9f44b-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="9f44b-441">(VIEW_TABLE_USAGE-Rowset)</span><span class="sxs-lookup"><span data-stu-id="9f44b-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9f44b-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9f44b-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="9f44b-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9f44b-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="9f44b-444">ANSICHTSNAME</span><span class="sxs-lookup"><span data-stu-id="9f44b-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9f44b-445">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="9f44b-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="9f44b-446">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9f44b-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f44b-447">Konstante</span><span class="sxs-lookup"><span data-stu-id="9f44b-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="9f44b-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="9f44b-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="9f44b-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="9f44b-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="9f44b-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="9f44b-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="9f44b-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="9f44b-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="9f44b-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="9f44b-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="9f44b-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="9f44b-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="9f44b-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="9f44b-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="9f44b-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="9f44b-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="9f44b-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="9f44b-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="9f44b-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="9f44b-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="9f44b-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="9f44b-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="9f44b-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f44b-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="9f44b-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9f44b-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="9f44b-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="9f44b-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="9f44b-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="9f44b-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="9f44b-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="9f44b-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="9f44b-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="9f44b-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="9f44b-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="9f44b-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="9f44b-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="9f44b-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="9f44b-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f44b-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="9f44b-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f44b-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="9f44b-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

