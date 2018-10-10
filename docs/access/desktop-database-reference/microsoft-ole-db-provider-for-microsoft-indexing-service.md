---
title: Microsoft OLE DB-Anbieter für Microsoft Indexdienst
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10af40231fc10e222f818896b3d65f44ac3d6d71
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473901"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="57156-102">Microsoft OLE DB-Anbieter für Microsoft Indexdienst</span><span class="sxs-lookup"><span data-stu-id="57156-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="57156-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="57156-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="57156-p101">Der Microsoft OLE DB-Anbieter für Microsoft Indexdienst ermöglicht den programmatischen schreibgeschützten Zugriff auf das Dateisystem sowie auf Webdaten, die vom Microsoft Indexdienst indiziert wurden. ADO-Anwendungen können SQL-Abfragen ausgeben, um Informationen zu Inhalts- und Dateieigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="57156-p101">The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and Web data indexed by Microsoft Indexing Service. ADO applications can issue SQL queries to retrieve content and file property information.</span></span>

<span data-ttu-id="57156-106">Der Anbieter ist ein Freethreadanbieter, der Unicode verwendet.</span><span class="sxs-lookup"><span data-stu-id="57156-106">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="57156-107">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="57156-107">Connection String Parameters</span></span>

<span data-ttu-id="57156-108">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das **Provider=** -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="57156-108">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="57156-109">Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="57156-109">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="57156-110">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57156-110">Typical Connection String</span></span>

<span data-ttu-id="57156-111">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="57156-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="57156-112">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="57156-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57156-113">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="57156-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="57156-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57156-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57156-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="57156-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="57156-p102">Gibt den OLE DB-Anbieter für Microsoft Indexdienst an. In der Regel ist dies das einzige Schlüsselwort, das in der Verbindungszeichenfolge angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="57156-p102">Specifies the OLE DB Provider for Microsoft Indexing Service. Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-118"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="57156-118"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="57156-p103">Gibt den Katalognamen des Indexdiensts an. Wenn dieses Schlüsselwort nicht angegeben ist, wird der Standardkatalog des Systems verwendet.</span><span class="sxs-lookup"><span data-stu-id="57156-p103">Specifies the Indexing Service catalog name. If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-121"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="57156-121"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="57156-p104">Gibt eine eindeutige 32-Bit-Zahl (z. B. 1033) an, mit der Einstellungen für die Sprache des Benutzers festgelegt werden. Diese Einstellungen geben an, wie Datum und Uhrzeit formatiert, Elemente alphabetisch sortiert, Zeichenfolgen verglichen werden usw. Wenn dieses Schlüsselwort nicht angegeben ist, wird die Standard-Gebietsschema-ID des Systems verwendet.</span><span class="sxs-lookup"><span data-stu-id="57156-p104">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on. If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="57156-125">Command Text</span><span class="sxs-lookup"><span data-stu-id="57156-125">Command Text</span></span>

<span data-ttu-id="57156-p105">Die Syntax für SQL-Abfragen des Indexdiensts besteht aus Erweiterungen der SQL-92 **SELECT** -Anweisung und deren Klauseln **FROM** und **WHERE**. Das Ergebnis der Abfrage wird mithilfe von OLE DB-Rowsets zurückgegeben, die von ADO verwendet werden und als [Recordset](recordset-object-ado.md)-Objekte geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="57156-p105">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses. The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="57156-p106">Sie können eine exakte Suche nach Wörtern oder Ausdrücken durchführen oder Platzhalter für die Suche nach Mustern oder Wortstämmen verwenden. Die Suchlogik kann auf booleschen Entscheidungen, gewichteten Ausdrücken oder Näherungen an andere Wörter basieren. Sie können auch eine Freitextsuche durchführen, mit der anstelle von Wortübereinstimmungen Bedeutungsübereinstimmungen gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="57156-p106">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words. The search logic can be based on Boolean decisions, weighted terms, or proximity to other words. You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="57156-131">Der Anbieter akzeptiert weder Aufrufe gespeicherter Prozeduren noch einfache Tabellennamen (die [CommandType](commandtype-property-ado.md)-Eigenschaft lautet beispielsweise immer **adCmdText**).</span><span class="sxs-lookup"><span data-stu-id="57156-131">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="57156-132">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="57156-132">Recordset Behavior</span></span>

<span data-ttu-id="57156-133">In den folgenden Tabellen sind die für ein **Recordset** -Objekt verfügbaren Features aufgeführt, das mit diesem Anbieter geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="57156-133">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="57156-134">Nur der statische Cursortyp (**AdOpenStatic**) zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="57156-134">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="57156-135">Ausführlichere Informationen zum **Recordset** -Verhalten Ihrer Anbieterkonfiguration erhalten Sie, wenn Sie die [Supports](supports-method-ado.md)-Methode ausführen und die [Properties](properties-collection-ado.md) -Auflistung des **Recordset** -Objekts aufzählen, um zu ermitteln, ob anbieterspezifische dynamische Eigenschaften vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="57156-135">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="57156-136">Verfügbarkeit von ADO-Standardeigenschaften des **Recordset** -Objekts:</span><span class="sxs-lookup"><span data-stu-id="57156-136">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57156-137">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57156-137">Property</span></span></p></th>
<th><p><span data-ttu-id="57156-138">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="57156-138">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57156-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="57156-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="57156-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57156-140">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="57156-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="57156-142">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57156-142">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="57156-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="57156-144">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="57156-144">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-145"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="57156-145"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="57156-146">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="57156-146">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-147"><a href="bookmark-property-ado.md">Lesezeichen</a>\*</span><span class="sxs-lookup"><span data-stu-id="57156-147"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="57156-148">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57156-148">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-149"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="57156-149"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="57156-150">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57156-150">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="57156-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="57156-152">immer <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="57156-152">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-153"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="57156-153"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="57156-154">immer <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="57156-154">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-155"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="57156-155"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="57156-156">immer <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="57156-156">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-157"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="57156-157"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="57156-158">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="57156-158">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-159"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="57156-159"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="57156-160">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57156-160">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-161"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="57156-161"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="57156-162">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57156-162">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="57156-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="57156-164">Nicht verf?gbar</span><span class="sxs-lookup"><span data-stu-id="57156-164">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="57156-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="57156-166">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57156-166">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-167"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="57156-167"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="57156-168">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="57156-168">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-169"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="57156-169"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="57156-170">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57156-170">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-171"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="57156-171"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="57156-172">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="57156-172">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-173"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="57156-173"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="57156-174">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57156-174">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-175"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="57156-175"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="57156-176">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="57156-176">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-177"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="57156-177"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="57156-178">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="57156-178">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57156-179">\*Lesezeichen müssen auf dem Anbieter für das **Recordset-Objekt**vorhanden ist damit dieses Feature aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="57156-179">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="57156-180">Verfügbarkeit von ADO-Standardmethoden des **Recordset** -Objekts:</span><span class="sxs-lookup"><span data-stu-id="57156-180">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57156-181">Methode</span><span class="sxs-lookup"><span data-stu-id="57156-181">Method</span></span></p></th>
<th><p><span data-ttu-id="57156-182">Verfügbar?</span><span class="sxs-lookup"><span data-stu-id="57156-182">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57156-183"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="57156-183"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="57156-184">Nein</span><span class="sxs-lookup"><span data-stu-id="57156-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-185"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="57156-185"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="57156-186">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="57156-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="57156-188">Nein</span><span class="sxs-lookup"><span data-stu-id="57156-188">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="57156-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="57156-190">Nein</span><span class="sxs-lookup"><span data-stu-id="57156-190">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-191"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="57156-191"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="57156-192">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-192">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-193"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="57156-193"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="57156-194">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-194">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-195"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="57156-195"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="57156-196">Nein</span><span class="sxs-lookup"><span data-stu-id="57156-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-197"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="57156-197"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="57156-198">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-199"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="57156-199"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="57156-200">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-200">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="57156-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="57156-202">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-202">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="57156-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="57156-204">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-205"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="57156-205"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="57156-206">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-207"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="57156-207"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="57156-208">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-208">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-209"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="57156-209"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="57156-210">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-211"><a href="supports-method-ado.md">Unterstützt</a></span><span class="sxs-lookup"><span data-stu-id="57156-211"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="57156-212">Ja</span><span class="sxs-lookup"><span data-stu-id="57156-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57156-213"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="57156-213"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="57156-214">Nein</span><span class="sxs-lookup"><span data-stu-id="57156-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57156-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="57156-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="57156-216">Nein</span><span class="sxs-lookup"><span data-stu-id="57156-216">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="57156-217">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57156-217">See also</span></span>

<span data-ttu-id="57156-218">Implementierung und funktionale Informationen zu den Microsoft OLE DB-Anbieter für Microsoft Indexdienst finden Sie in der Microsoft OLE DB Programmer's Reference.</span><span class="sxs-lookup"><span data-stu-id="57156-218">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

