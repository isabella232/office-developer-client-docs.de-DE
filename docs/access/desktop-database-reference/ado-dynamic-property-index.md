---
title: Index zu dynamischen ADO-Eigenschaften
TOCTitle: ADO Dynamic Property Index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58e9029e7c78a6cbde97973ee7fc482fb116c3f2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473014"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="2277c-102">Index zu dynamischen ADO-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2277c-102">ADO Dynamic Property Index</span></span>


<span data-ttu-id="2277c-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2277c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2277c-p101">Datenprovider, Dienstanbieter und Dienstkomponenten können den **Properties** -Auflistungen der nicht geöffneten Objekte [Connection](connection-object-ado.md) und [Recordset](recordset-object-ado.md) dynamische Eigenschaften hinzufügen. Ein bestimmter Anbieter kann möglicherweise auch zusätzliche Eigenschaften hinzufügen, wenn diese Objekte geöffnet sind. Einige dieser Eigenschaften sind im Abschnitt " [Dynamische ADO-Eigenschaften](ado-dynamic-properties.md)" aufgeführt. Weitere sind unter den jeweiligen Anbietern im Abschnitt "[Anhang A: Anbieter](appendix-a-providers.md)" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2277c-p101">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects. A given provider may also insert additional properties when these objects are opened. Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section. More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="2277c-p102">Bei der folgenden Tabelle handelt es sich um ein Cross-Index-System der ADO- und OLE DB-Namen für alle dynamischen Standardeigenschaften von OLE DB-Anbietern. Die Anbieter können mehr als die hier aufgeführten Eigenschaften hinzufügen. Gezielte Informationen zu anbieterspezifischen dynamischen Eigenschaften finden Sie in der Dokumentation zum Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2277c-p102">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property. Your providers may add more properties than listed here. For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="2277c-p103">In OLE DB Programmer's Reference wird ein ADO-Eigenschaftenname als "Description" bezeichnet. Weitere Informationen zu diesen Standardeigenschaften finden Sie in OLE DB Programmer's Reference. Suchen Sie im Index nach dem OLE DB-Eigenschaftennamen, oder lesen Sie die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="2277c-p103">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these standard properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see the following topics:</span></span>

  - <span data-ttu-id="2277c-114">Appendix C: OLE DB Properties (in Englisch)</span><span class="sxs-lookup"><span data-stu-id="2277c-114">Appendix C: OLE DB Properties</span></span>

  - <span data-ttu-id="2277c-115">Supported Properties of the Cursor Service (in Englisch)</span><span class="sxs-lookup"><span data-stu-id="2277c-115">Supported Properties of the Cursor Service</span></span>

  - <span data-ttu-id="2277c-116">Supported Properties of the Persistence Provider (in Englisch)</span><span class="sxs-lookup"><span data-stu-id="2277c-116">Supported Properties of the Persistence Provider</span></span>

  - <span data-ttu-id="2277c-117">Supported OLE DB Properties of the Remoting Provider (in Englisch)</span><span class="sxs-lookup"><span data-stu-id="2277c-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="2277c-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2277c-118">Remarks</span></span>

<span data-ttu-id="2277c-119">Im Cross-Index verwendete Nummern:</span><span class="sxs-lookup"><span data-stu-id="2277c-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="2277c-p104">(1) Bei dieser Eigenschaft handelt es sich um ein boolesches Flag, das angibt, ob die benannte Schnittstelle verwendet werden soll. Sofern vorhanden, ist der entsprechende OLE DB-Eigenschaftenname aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2277c-p104">(1) This property is a Boolean flag indicating whether the named interface should be used. The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="2277c-122">(2) die "Bookmarkable" ADO-Eigenschaft wird intern generiert für Abwärtskompatibilität Kompatibilität und der OLE DB-Eigenschaft DBPROP zugeordnet\_IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="2277c-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="2277c-123">Dies ist die gleiche Eigenschaft, die die ADO-Eigenschaft IRowsetLocate entspricht.</span><span class="sxs-lookup"><span data-stu-id="2277c-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="2277c-124">(3) Der ADO-Eigenschaftenname Hidden Columns ist anders benannt als die Beschreibung des OLE DB-Eigenschaftennamens Hidden Columns Count.</span><span class="sxs-lookup"><span data-stu-id="2277c-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="2277c-p106">(4) Bei hierarchischen Datensatzgruppen wird die ADO-Eigenschaft Maximum Rows auf alle untergeordneten Datensatzgruppen angewendet. Je nach Reihenfolge, in der die Zeilen zurückgegeben werden, befinden sich in der Ergebnisgruppe für die einzelnen übergeordneten Gruppen alle, einige oder keine untergeordneten Gruppen oder verwaiste untergeordnete Gruppen. Daher muss die Kennung für die einzelnen untergeordneten Gruppen beim Umstrukturieren hierarchischer Datensatzgruppen eindeutig sein. Der Anbieter Microsoft Data Shaping Service for OLE DB (MSDATASHAPE) ermöglicht generell keine Unterscheidung zwischen Eigenschaften, die von der übergeordneten Gruppe vererbt werden können, und denjenigen, die nicht vererbt werden können.</span><span class="sxs-lookup"><span data-stu-id="2277c-p106">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children. Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set. Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique. In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="2277c-129">(5) Nicht zutreffend.</span><span class="sxs-lookup"><span data-stu-id="2277c-129">(5) Does not apply.</span></span>

<span data-ttu-id="2277c-130">**Dynamische Eigenschaften von "Connection"**</span><span class="sxs-lookup"><span data-stu-id="2277c-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2277c-131">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="2277c-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="2277c-132">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="2277c-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2277c-133">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="2277c-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="2277c-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="2277c-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="2277c-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="2277c-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="2277c-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="2277c-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="2277c-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="2277c-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-139">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="2277c-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="2277c-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="2277c-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-141">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="2277c-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="2277c-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="2277c-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-143">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="2277c-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="2277c-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="2277c-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-145">Column Definition</span><span class="sxs-lookup"><span data-stu-id="2277c-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="2277c-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="2277c-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-147">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="2277c-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="2277c-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2277c-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-149">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="2277c-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="2277c-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="2277c-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-151">Data Source</span><span class="sxs-lookup"><span data-stu-id="2277c-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="2277c-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="2277c-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-153">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="2277c-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="2277c-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="2277c-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-155">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="2277c-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="2277c-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="2277c-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="2277c-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="2277c-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="2277c-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-159">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="2277c-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="2277c-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="2277c-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-161">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="2277c-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="2277c-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="2277c-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-163">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="2277c-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="2277c-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="2277c-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-165">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="2277c-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="2277c-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="2277c-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-167">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="2277c-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="2277c-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="2277c-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-169">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="2277c-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="2277c-170">NULL</span><span class="sxs-lookup"><span data-stu-id="2277c-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-171">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="2277c-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="2277c-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="2277c-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-173">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="2277c-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="2277c-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="2277c-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-175">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="2277c-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="2277c-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="2277c-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-177">Location</span><span class="sxs-lookup"><span data-stu-id="2277c-177">Location</span></span></p></td>
<td><p><span data-ttu-id="2277c-178">STANDARD</span><span class="sxs-lookup"><span data-stu-id="2277c-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-179">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="2277c-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="2277c-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="2277c-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-181">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="2277c-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="2277c-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="2277c-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-183">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="2277c-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="2277c-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="2277c-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-185">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="2277c-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="2277c-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="2277c-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-187">Mode</span><span class="sxs-lookup"><span data-stu-id="2277c-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="2277c-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="2277c-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-189">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="2277c-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="2277c-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="2277c-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-191">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="2277c-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="2277c-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="2277c-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-193">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="2277c-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="2277c-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="2277c-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-195">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="2277c-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="2277c-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="2277c-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-197">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="2277c-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="2277c-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="2277c-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-199">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="2277c-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="2277c-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="2277c-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-201">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="2277c-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="2277c-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="2277c-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-203">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="2277c-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="2277c-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="2277c-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-205">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="2277c-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="2277c-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="2277c-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-207">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="2277c-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="2277c-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="2277c-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="2277c-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="2277c-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="2277c-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-211">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="2277c-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="2277c-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="2277c-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="2277c-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="2277c-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="2277c-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-215">Password</span><span class="sxs-lookup"><span data-stu-id="2277c-215">Password</span></span></p></td>
<td><p><span data-ttu-id="2277c-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="2277c-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-217">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="2277c-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="2277c-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="2277c-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-219">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="2277c-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="2277c-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="2277c-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-221">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="2277c-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="2277c-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="2277c-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-223">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="2277c-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="2277c-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="2277c-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-225">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="2277c-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="2277c-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="2277c-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="2277c-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="2277c-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="2277c-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-229">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="2277c-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="2277c-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="2277c-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-231">Provider Name</span><span class="sxs-lookup"><span data-stu-id="2277c-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="2277c-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="2277c-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-233">Provider Version</span><span class="sxs-lookup"><span data-stu-id="2277c-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="2277c-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="2277c-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-235">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="2277c-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="2277c-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="2277c-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-237">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="2277c-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="2277c-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="2277c-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-239">Schema Term</span><span class="sxs-lookup"><span data-stu-id="2277c-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="2277c-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="2277c-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-241">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="2277c-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="2277c-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="2277c-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-243">SQL Support</span><span class="sxs-lookup"><span data-stu-id="2277c-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="2277c-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="2277c-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-245">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="2277c-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="2277c-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="2277c-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-247">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="2277c-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="2277c-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="2277c-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="2277c-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="2277c-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="2277c-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-251">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="2277c-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="2277c-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="2277c-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-253">User ID</span><span class="sxs-lookup"><span data-stu-id="2277c-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="2277c-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="2277c-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-255">User Name</span><span class="sxs-lookup"><span data-stu-id="2277c-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="2277c-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="2277c-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-257">Window Handle</span><span class="sxs-lookup"><span data-stu-id="2277c-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="2277c-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="2277c-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2277c-259">**Dynamische Eigenschaften von "Recordset"**</span><span class="sxs-lookup"><span data-stu-id="2277c-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="2277c-260">Die **dynamischen Eigenschaften** des **Recordset** -Objekts sind nicht mehr verfügbar, wenn das **Recordset** -Objekt geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="2277c-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2277c-261">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="2277c-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="2277c-262">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="2277c-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2277c-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="2277c-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="2277c-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="2277c-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="2277c-266">(1)</span><span class="sxs-lookup"><span data-stu-id="2277c-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="2277c-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="2277c-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="2277c-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="2277c-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="2277c-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="2277c-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="2277c-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="2277c-274">(1)</span><span class="sxs-lookup"><span data-stu-id="2277c-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="2277c-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="2277c-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="2277c-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="2277c-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="2277c-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="2277c-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="2277c-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="2277c-282">(1)</span><span class="sxs-lookup"><span data-stu-id="2277c-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="2277c-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="2277c-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="2277c-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="2277c-286">(1)</span><span class="sxs-lookup"><span data-stu-id="2277c-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="2277c-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="2277c-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="2277c-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="2277c-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="2277c-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="2277c-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="2277c-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="2277c-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-295">IRowsetRefresh abgelöst</span><span class="sxs-lookup"><span data-stu-id="2277c-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="2277c-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="2277c-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="2277c-298">(1)</span><span class="sxs-lookup"><span data-stu-id="2277c-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="2277c-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="2277c-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="2277c-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="2277c-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="2277c-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="2277c-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="2277c-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="2277c-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="2277c-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="2277c-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="2277c-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="2277c-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-311">IStream</span><span class="sxs-lookup"><span data-stu-id="2277c-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="2277c-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="2277c-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="2277c-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="2277c-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-315">Access Order</span><span class="sxs-lookup"><span data-stu-id="2277c-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="2277c-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="2277c-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="2277c-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="2277c-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="2277c-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-319">Asynchronous Rowset Processing</span><span class="sxs-lookup"><span data-stu-id="2277c-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="2277c-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="2277c-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-321">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="2277c-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="2277c-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="2277c-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-323">Background Fetch Size</span><span class="sxs-lookup"><span data-stu-id="2277c-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="2277c-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="2277c-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-325">Background Thread Priority</span><span class="sxs-lookup"><span data-stu-id="2277c-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="2277c-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="2277c-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-327">Batch Size</span><span class="sxs-lookup"><span data-stu-id="2277c-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="2277c-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="2277c-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-329">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="2277c-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="2277c-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="2277c-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-331">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="2277c-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="2277c-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="2277c-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="2277c-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="2277c-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="2277c-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="2277c-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="2277c-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="2277c-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-337">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="2277c-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="2277c-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="2277c-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-339">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="2277c-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="2277c-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="2277c-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-341">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="2277c-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="2277c-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="2277c-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-343">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="2277c-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="2277c-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="2277c-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-345">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="2277c-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-347">Column Writable</span><span class="sxs-lookup"><span data-stu-id="2277c-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="2277c-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="2277c-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-349">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="2277c-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="2277c-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2277c-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-351">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="2277c-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="2277c-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="2277c-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-353">Defer Column</span><span class="sxs-lookup"><span data-stu-id="2277c-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="2277c-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="2277c-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-355">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="2277c-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="2277c-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="2277c-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="2277c-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="2277c-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="2277c-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-359">Filter Operations</span><span class="sxs-lookup"><span data-stu-id="2277c-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="2277c-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="2277c-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-361">Find Operations</span><span class="sxs-lookup"><span data-stu-id="2277c-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="2277c-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="2277c-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-363">Hidden Columns (Count)</span><span class="sxs-lookup"><span data-stu-id="2277c-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="2277c-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="2277c-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-365">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="2277c-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="2277c-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="2277c-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="2277c-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="2277c-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="2277c-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-369">Initial Fetch Size</span><span class="sxs-lookup"><span data-stu-id="2277c-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="2277c-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="2277c-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-371">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="2277c-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="2277c-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="2277c-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-373">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="2277c-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="2277c-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="2277c-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-375">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="2277c-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="2277c-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="2277c-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-377">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="2277c-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="2277c-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="2277c-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-379">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="2277c-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="2277c-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="2277c-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-381">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="2277c-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="2277c-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="2277c-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-383">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="2277c-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="2277c-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="2277c-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-385">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="2277c-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="2277c-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="2277c-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-387">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="2277c-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="2277c-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="2277c-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="2277c-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="2277c-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="2277c-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-391">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="2277c-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="2277c-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="2277c-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-393">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="2277c-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="2277c-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="2277c-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-395">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="2277c-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="2277c-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="2277c-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-397">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="2277c-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="2277c-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="2277c-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-399">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="2277c-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="2277c-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="2277c-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-401">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="2277c-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="2277c-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="2277c-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-403">Private1</span><span class="sxs-lookup"><span data-stu-id="2277c-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="2277c-404">(5)</span><span class="sxs-lookup"><span data-stu-id="2277c-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-405">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="2277c-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="2277c-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="2277c-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="2277c-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="2277c-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="2277c-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-409">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="2277c-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="2277c-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="2277c-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-411">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="2277c-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="2277c-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="2277c-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="2277c-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="2277c-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="2277c-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="2277c-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="2277c-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="2277c-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-417">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="2277c-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="2277c-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="2277c-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-419">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="2277c-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-421">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="2277c-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-423">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="2277c-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-425">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="2277c-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="2277c-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="2277c-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-427">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="2277c-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-429">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="2277c-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="2277c-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="2277c-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-431">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="2277c-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-433">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="2277c-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-435">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="2277c-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-437">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="2277c-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="2277c-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-441">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="2277c-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="2277c-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="2277c-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-443">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="2277c-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="2277c-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="2277c-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-445">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="2277c-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="2277c-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="2277c-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-447">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="2277c-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="2277c-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="2277c-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-449">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="2277c-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="2277c-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="2277c-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-451">Unique Catalog</span><span class="sxs-lookup"><span data-stu-id="2277c-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="2277c-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="2277c-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-453">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="2277c-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="2277c-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="2277c-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-455">Unique Schema</span><span class="sxs-lookup"><span data-stu-id="2277c-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="2277c-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="2277c-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-457">Unique Table</span><span class="sxs-lookup"><span data-stu-id="2277c-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="2277c-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="2277c-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="2277c-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="2277c-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="2277c-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-461">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="2277c-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="2277c-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="2277c-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2277c-463">Update Resync</span><span class="sxs-lookup"><span data-stu-id="2277c-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="2277c-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="2277c-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2277c-465">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="2277c-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="2277c-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="2277c-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

