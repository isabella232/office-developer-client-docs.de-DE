---
title: Index zu dynamischen ADO-Eigenschaften
TOCTitle: ADO Dynamic Property Index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f385f3637f9a64ff94d571345d88fbaa088d126
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876064"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="6cddc-102">Index zu dynamischen ADO-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6cddc-102">ADO Dynamic Property Index</span></span>


<span data-ttu-id="6cddc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6cddc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6cddc-p101">Datenprovider, Dienstanbieter und Dienstkomponenten können den **Properties** -Auflistungen der nicht geöffneten Objekte [Connection](connection-object-ado.md) und [Recordset](recordset-object-ado.md) dynamische Eigenschaften hinzufügen. Ein bestimmter Anbieter kann möglicherweise auch zusätzliche Eigenschaften hinzufügen, wenn diese Objekte geöffnet sind. Einige dieser Eigenschaften sind im Abschnitt " [Dynamische ADO-Eigenschaften](ado-dynamic-properties.md)" aufgeführt. Weitere sind unter den jeweiligen Anbietern im Abschnitt "[Anhang A: Anbieter](appendix-a-providers.md)" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cddc-p101">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects. A given provider may also insert additional properties when these objects are opened. Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section. More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="6cddc-p102">Bei der folgenden Tabelle handelt es sich um ein Cross-Index-System der ADO- und OLE DB-Namen für alle dynamischen Standardeigenschaften von OLE DB-Anbietern. Die Anbieter können mehr als die hier aufgeführten Eigenschaften hinzufügen. Gezielte Informationen zu anbieterspezifischen dynamischen Eigenschaften finden Sie in der Dokumentation zum Anbieter.</span><span class="sxs-lookup"><span data-stu-id="6cddc-p102">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property. Your providers may add more properties than listed here. For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="6cddc-p103">In OLE DB Programmer's Reference wird ein ADO-Eigenschaftenname als "Description" bezeichnet. Weitere Informationen zu diesen Standardeigenschaften finden Sie in OLE DB Programmer's Reference. Suchen Sie im Index nach dem OLE DB-Eigenschaftennamen, oder lesen Sie die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6cddc-p103">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these standard properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see the following topics:</span></span>

  - <span data-ttu-id="6cddc-114">Appendix C: OLE DB Properties (in Englisch)</span><span class="sxs-lookup"><span data-stu-id="6cddc-114">Appendix C: OLE DB Properties</span></span>

  - <span data-ttu-id="6cddc-115">Supported Properties of the Cursor Service (in Englisch)</span><span class="sxs-lookup"><span data-stu-id="6cddc-115">Supported Properties of the Cursor Service</span></span>

  - <span data-ttu-id="6cddc-116">Supported Properties of the Persistence Provider (in Englisch)</span><span class="sxs-lookup"><span data-stu-id="6cddc-116">Supported Properties of the Persistence Provider</span></span>

  - <span data-ttu-id="6cddc-117">Supported OLE DB Properties of the Remoting Provider (in Englisch)</span><span class="sxs-lookup"><span data-stu-id="6cddc-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="6cddc-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6cddc-118">Remarks</span></span>

<span data-ttu-id="6cddc-119">Im Cross-Index verwendete Nummern:</span><span class="sxs-lookup"><span data-stu-id="6cddc-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="6cddc-p104">(1) Bei dieser Eigenschaft handelt es sich um ein boolesches Flag, das angibt, ob die benannte Schnittstelle verwendet werden soll. Sofern vorhanden, ist der entsprechende OLE DB-Eigenschaftenname aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cddc-p104">(1) This property is a Boolean flag indicating whether the named interface should be used. The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="6cddc-122">(2) die "Bookmarkable" ADO-Eigenschaft wird intern generiert für Abwärtskompatibilität Kompatibilität und der OLE DB-Eigenschaft DBPROP zugeordnet\_IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="6cddc-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="6cddc-123">Dies ist die gleiche Eigenschaft, die die ADO-Eigenschaft IRowsetLocate entspricht.</span><span class="sxs-lookup"><span data-stu-id="6cddc-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="6cddc-124">(3) Der ADO-Eigenschaftenname Hidden Columns ist anders benannt als die Beschreibung des OLE DB-Eigenschaftennamens Hidden Columns Count.</span><span class="sxs-lookup"><span data-stu-id="6cddc-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="6cddc-p106">(4) Bei hierarchischen Datensatzgruppen wird die ADO-Eigenschaft Maximum Rows auf alle untergeordneten Datensatzgruppen angewendet. Je nach Reihenfolge, in der die Zeilen zurückgegeben werden, befinden sich in der Ergebnisgruppe für die einzelnen übergeordneten Gruppen alle, einige oder keine untergeordneten Gruppen oder verwaiste untergeordnete Gruppen. Daher muss die Kennung für die einzelnen untergeordneten Gruppen beim Umstrukturieren hierarchischer Datensatzgruppen eindeutig sein. Der Anbieter Microsoft Data Shaping Service for OLE DB (MSDATASHAPE) ermöglicht generell keine Unterscheidung zwischen Eigenschaften, die von der übergeordneten Gruppe vererbt werden können, und denjenigen, die nicht vererbt werden können.</span><span class="sxs-lookup"><span data-stu-id="6cddc-p106">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children. Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set. Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique. In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="6cddc-129">(5) Nicht zutreffend.</span><span class="sxs-lookup"><span data-stu-id="6cddc-129">(5) Does not apply.</span></span>

<span data-ttu-id="6cddc-130">**Dynamische Eigenschaften von "Connection"**</span><span class="sxs-lookup"><span data-stu-id="6cddc-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cddc-131">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="6cddc-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="6cddc-132">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="6cddc-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-133">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="6cddc-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="6cddc-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="6cddc-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="6cddc-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="6cddc-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="6cddc-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="6cddc-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="6cddc-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="6cddc-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-139">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="6cddc-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="6cddc-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="6cddc-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-141">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="6cddc-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="6cddc-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="6cddc-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-143">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="6cddc-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="6cddc-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="6cddc-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-145">Column Definition</span><span class="sxs-lookup"><span data-stu-id="6cddc-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="6cddc-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="6cddc-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-147">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="6cddc-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="6cddc-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6cddc-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-149">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="6cddc-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="6cddc-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="6cddc-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-151">Data Source</span><span class="sxs-lookup"><span data-stu-id="6cddc-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="6cddc-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="6cddc-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-153">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="6cddc-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="6cddc-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="6cddc-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-155">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="6cddc-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="6cddc-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="6cddc-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="6cddc-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="6cddc-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="6cddc-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-159">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="6cddc-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="6cddc-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="6cddc-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-161">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="6cddc-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="6cddc-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="6cddc-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-163">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="6cddc-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="6cddc-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="6cddc-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-165">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="6cddc-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="6cddc-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="6cddc-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-167">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="6cddc-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="6cddc-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="6cddc-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-169">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="6cddc-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="6cddc-170">NULL</span><span class="sxs-lookup"><span data-stu-id="6cddc-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-171">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="6cddc-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="6cddc-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="6cddc-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-173">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="6cddc-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="6cddc-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="6cddc-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-175">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="6cddc-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="6cddc-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="6cddc-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-177">Location</span><span class="sxs-lookup"><span data-stu-id="6cddc-177">Location</span></span></p></td>
<td><p><span data-ttu-id="6cddc-178">STANDARD</span><span class="sxs-lookup"><span data-stu-id="6cddc-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-179">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="6cddc-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="6cddc-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="6cddc-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-181">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="6cddc-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="6cddc-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="6cddc-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-183">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="6cddc-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="6cddc-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="6cddc-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-185">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="6cddc-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="6cddc-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="6cddc-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-187">Mode</span><span class="sxs-lookup"><span data-stu-id="6cddc-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="6cddc-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="6cddc-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-189">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="6cddc-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="6cddc-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="6cddc-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-191">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="6cddc-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="6cddc-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="6cddc-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-193">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="6cddc-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="6cddc-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6cddc-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-195">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="6cddc-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="6cddc-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="6cddc-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-197">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="6cddc-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="6cddc-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="6cddc-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-199">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="6cddc-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="6cddc-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="6cddc-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-201">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="6cddc-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="6cddc-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="6cddc-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-203">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="6cddc-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="6cddc-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="6cddc-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-205">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="6cddc-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="6cddc-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6cddc-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-207">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="6cddc-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="6cddc-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="6cddc-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="6cddc-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="6cddc-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="6cddc-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-211">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="6cddc-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="6cddc-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="6cddc-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="6cddc-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="6cddc-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="6cddc-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-215">Password</span><span class="sxs-lookup"><span data-stu-id="6cddc-215">Password</span></span></p></td>
<td><p><span data-ttu-id="6cddc-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="6cddc-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-217">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="6cddc-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="6cddc-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="6cddc-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-219">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="6cddc-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="6cddc-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="6cddc-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-221">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="6cddc-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="6cddc-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="6cddc-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-223">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="6cddc-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="6cddc-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="6cddc-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-225">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="6cddc-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="6cddc-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="6cddc-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="6cddc-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="6cddc-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="6cddc-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-229">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="6cddc-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="6cddc-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="6cddc-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-231">Provider Name</span><span class="sxs-lookup"><span data-stu-id="6cddc-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="6cddc-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="6cddc-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-233">Provider Version</span><span class="sxs-lookup"><span data-stu-id="6cddc-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="6cddc-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="6cddc-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-235">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="6cddc-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="6cddc-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="6cddc-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-237">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="6cddc-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="6cddc-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="6cddc-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-239">Schema Term</span><span class="sxs-lookup"><span data-stu-id="6cddc-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="6cddc-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="6cddc-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-241">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="6cddc-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="6cddc-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="6cddc-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-243">SQL Support</span><span class="sxs-lookup"><span data-stu-id="6cddc-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="6cddc-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="6cddc-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-245">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="6cddc-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="6cddc-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="6cddc-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-247">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="6cddc-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="6cddc-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="6cddc-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="6cddc-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="6cddc-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="6cddc-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-251">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="6cddc-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="6cddc-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="6cddc-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-253">User ID</span><span class="sxs-lookup"><span data-stu-id="6cddc-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="6cddc-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="6cddc-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-255">User Name</span><span class="sxs-lookup"><span data-stu-id="6cddc-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="6cddc-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="6cddc-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-257">Window Handle</span><span class="sxs-lookup"><span data-stu-id="6cddc-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="6cddc-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="6cddc-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6cddc-259">**Dynamische Eigenschaften von "Recordset"**</span><span class="sxs-lookup"><span data-stu-id="6cddc-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="6cddc-260">Die **dynamischen Eigenschaften** des **Recordset** -Objekts sind nicht mehr verfügbar, wenn das **Recordset** -Objekt geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="6cddc-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cddc-261">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="6cddc-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="6cddc-262">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="6cddc-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="6cddc-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="6cddc-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="6cddc-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="6cddc-266">(1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="6cddc-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="6cddc-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="6cddc-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="6cddc-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="6cddc-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="6cddc-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="6cddc-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="6cddc-274">(1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="6cddc-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="6cddc-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="6cddc-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="6cddc-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="6cddc-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="6cddc-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="6cddc-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="6cddc-282">(1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="6cddc-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="6cddc-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="6cddc-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="6cddc-286">(1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="6cddc-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="6cddc-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="6cddc-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="6cddc-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="6cddc-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="6cddc-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="6cddc-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="6cddc-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-295">IRowsetRefresh abgelöst</span><span class="sxs-lookup"><span data-stu-id="6cddc-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="6cddc-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="6cddc-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="6cddc-298">(1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="6cddc-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="6cddc-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="6cddc-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="6cddc-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="6cddc-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="6cddc-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="6cddc-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="6cddc-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="6cddc-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="6cddc-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="6cddc-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="6cddc-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-311">IStream</span><span class="sxs-lookup"><span data-stu-id="6cddc-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="6cddc-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="6cddc-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="6cddc-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="6cddc-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-315">Access Order</span><span class="sxs-lookup"><span data-stu-id="6cddc-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="6cddc-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="6cddc-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="6cddc-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="6cddc-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="6cddc-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-319">Asynchronous Rowset Processing</span><span class="sxs-lookup"><span data-stu-id="6cddc-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="6cddc-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="6cddc-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-321">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="6cddc-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="6cddc-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="6cddc-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-323">Background Fetch Size</span><span class="sxs-lookup"><span data-stu-id="6cddc-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="6cddc-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="6cddc-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-325">Background Thread Priority</span><span class="sxs-lookup"><span data-stu-id="6cddc-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="6cddc-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="6cddc-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-327">Batch Size</span><span class="sxs-lookup"><span data-stu-id="6cddc-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="6cddc-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="6cddc-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-329">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="6cddc-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="6cddc-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6cddc-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-331">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="6cddc-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="6cddc-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="6cddc-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="6cddc-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="6cddc-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="6cddc-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="6cddc-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="6cddc-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6cddc-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-337">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="6cddc-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="6cddc-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="6cddc-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-339">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="6cddc-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="6cddc-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="6cddc-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-341">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="6cddc-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="6cddc-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="6cddc-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-343">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="6cddc-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="6cddc-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="6cddc-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-345">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="6cddc-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-347">Column Writable</span><span class="sxs-lookup"><span data-stu-id="6cddc-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="6cddc-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6cddc-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-349">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="6cddc-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="6cddc-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6cddc-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-351">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="6cddc-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="6cddc-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="6cddc-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-353">Defer Column</span><span class="sxs-lookup"><span data-stu-id="6cddc-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="6cddc-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="6cddc-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-355">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="6cddc-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="6cddc-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6cddc-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="6cddc-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="6cddc-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="6cddc-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-359">Filter Operations</span><span class="sxs-lookup"><span data-stu-id="6cddc-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="6cddc-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="6cddc-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-361">Find Operations</span><span class="sxs-lookup"><span data-stu-id="6cddc-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="6cddc-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="6cddc-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-363">Hidden Columns (Count)</span><span class="sxs-lookup"><span data-stu-id="6cddc-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="6cddc-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="6cddc-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-365">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="6cddc-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="6cddc-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="6cddc-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="6cddc-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="6cddc-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="6cddc-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-369">Initial Fetch Size</span><span class="sxs-lookup"><span data-stu-id="6cddc-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="6cddc-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="6cddc-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-371">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="6cddc-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6cddc-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6cddc-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-373">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="6cddc-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6cddc-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="6cddc-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-375">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="6cddc-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="6cddc-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="6cddc-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-377">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="6cddc-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="6cddc-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="6cddc-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-379">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="6cddc-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="6cddc-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="6cddc-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-381">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="6cddc-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="6cddc-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="6cddc-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-383">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="6cddc-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="6cddc-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="6cddc-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-385">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="6cddc-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="6cddc-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="6cddc-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-387">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="6cddc-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="6cddc-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="6cddc-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="6cddc-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="6cddc-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="6cddc-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-391">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="6cddc-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6cddc-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="6cddc-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-393">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="6cddc-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6cddc-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="6cddc-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-395">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="6cddc-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6cddc-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="6cddc-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-397">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="6cddc-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6cddc-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="6cddc-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-399">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="6cddc-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="6cddc-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="6cddc-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-401">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="6cddc-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="6cddc-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="6cddc-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-403">Private1</span><span class="sxs-lookup"><span data-stu-id="6cddc-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="6cddc-404">(5)</span><span class="sxs-lookup"><span data-stu-id="6cddc-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-405">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="6cddc-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="6cddc-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="6cddc-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="6cddc-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="6cddc-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="6cddc-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-409">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="6cddc-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="6cddc-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="6cddc-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-411">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="6cddc-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="6cddc-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="6cddc-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="6cddc-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="6cddc-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="6cddc-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="6cddc-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="6cddc-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="6cddc-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-417">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="6cddc-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="6cddc-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="6cddc-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-419">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="6cddc-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-421">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="6cddc-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-423">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="6cddc-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-425">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="6cddc-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="6cddc-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="6cddc-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-427">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="6cddc-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-429">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="6cddc-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="6cddc-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="6cddc-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-431">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="6cddc-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-433">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="6cddc-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-435">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="6cddc-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-437">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="6cddc-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="6cddc-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-441">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="6cddc-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="6cddc-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="6cddc-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-443">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="6cddc-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="6cddc-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="6cddc-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-445">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="6cddc-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="6cddc-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="6cddc-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-447">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="6cddc-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6cddc-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="6cddc-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-449">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="6cddc-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6cddc-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="6cddc-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-451">Unique Catalog</span><span class="sxs-lookup"><span data-stu-id="6cddc-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="6cddc-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="6cddc-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-453">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="6cddc-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="6cddc-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="6cddc-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-455">Unique Schema</span><span class="sxs-lookup"><span data-stu-id="6cddc-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="6cddc-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="6cddc-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-457">Unique Table</span><span class="sxs-lookup"><span data-stu-id="6cddc-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="6cddc-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="6cddc-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="6cddc-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="6cddc-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="6cddc-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-461">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="6cddc-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="6cddc-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="6cddc-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cddc-463">Update Resync</span><span class="sxs-lookup"><span data-stu-id="6cddc-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="6cddc-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="6cddc-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cddc-465">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="6cddc-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6cddc-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6cddc-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

