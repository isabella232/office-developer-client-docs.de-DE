---
title: Microsoft Cursor Service für OLE DB (ADO-Dienstkomponente)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 175023f12d1efa23422afb15e693d44976421cc0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473480"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a><span data-ttu-id="2102c-102">Microsoft Cursor Service für OLE DB (ADO-Dienstkomponente)</span><span class="sxs-lookup"><span data-stu-id="2102c-102">Microsoft Cursor Service for OLE DB (ADO Service Component)</span></span>


<span data-ttu-id="2102c-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2102c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2102c-p101">Der Microsoft Cursor Service für OLE DB ergänzt die Cursor-Hilfsfunktionen von Datenanbietern. Der Benutzer nimmt daher eine relativ einheitliche Funktionalität aller Datenprovider wahr.</span><span class="sxs-lookup"><span data-stu-id="2102c-p101">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers. As a result, the user perceives relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="2102c-p102">Der Cursordienst macht dynamische Eigenschaften verfügbar und verbessert das Verhalten bestimmter Methoden. Beispiel: Die dynamische [Optimize](optimize-property-dynamic-ado.md)-Eigenschaft ermöglicht das Erstellen temporärer Indizes, um bestimmte Vorgänge, wie die [Find](find-method-ado.md)-Methode, zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="2102c-p102">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods. For example, the [Optimize](optimize-property-dynamic-ado.md) dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the [Find](find-method-ado.md) method.</span></span>

<span data-ttu-id="2102c-p103">Der Cursordienst ermöglicht die Unterstützung von Batchaktualisierungen in allen Fällen. Er simuliert darüber hinaus auch leistungsfähigere Cursortypen, wie dynamische Cursor, wenn ein Datenprovider nur weniger leistungsfähige Cursor, wie statische Cursor, bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="2102c-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

## <a name="keyword"></a><span data-ttu-id="2102c-110">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="2102c-110">Keyword</span></span>

<span data-ttu-id="2102c-111">Um diese Dienstkomponente aufzurufen, legen Sie die [CursorLocation](recordset-object-ado.md)-Eigenschaft der Objekte [Recordset](connection-object-ado.md) oder [Connection](cursorlocation-property-ado.md) auf **adUseClient** fest.</span><span class="sxs-lookup"><span data-stu-id="2102c-111">To invoke this service component, set the [Recordset](recordset-object-ado.md) or [Connection](connection-object-ado.md) object's [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a><span data-ttu-id="2102c-112">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2102c-112">Dynamic Properties</span></span>

<span data-ttu-id="2102c-p104">Wenn der Microsoft Cursor Service für OLE DB aufgerufen wird, werden der **Properties**-Auflistung des [Recordset](properties-collection-ado.md) -Objekts die folgenden dynamischen Eigenschaften hinzugefügt. Eine vollständige Liste mit den dynamischen Eigenschaften der Objekte **Connection** und **Recordset** finden Sie im [Index zu dynamischen ADO-Eigenschaften](ado-dynamic-property-index.md). Die zugehörigen OLE DB-Eigenschaftennamen sind ggf. nach den ADO-Eigenschaftennamen in Klammern angegeben.</span><span class="sxs-lookup"><span data-stu-id="2102c-p104">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the **Recordset** object's [Properties](properties-collection-ado.md) collection. The full list of **Connection** and **Recordset** object dynamic properties is listed in the [ADO Dynamic Property Index](ado-dynamic-property-index.md). The associated OLE DB property names, where appropriate, are included in parenthesis after the ADO property name.</span></span>

<span data-ttu-id="2102c-116">Nach dem Aufrufen des Cursordiensts sind Änderungen an einigen dynamischen Eigenschaften für die zugrunde liegende Datenquelle nicht erkennbar.</span><span class="sxs-lookup"><span data-stu-id="2102c-116">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked.</span></span> <span data-ttu-id="2102c-117">Beispielsweise wird durch Festlegen der *Befehl Zeitlimit* -Eigenschaft für ein **Recordset-Objekt** für die zugrunde liegenden Datenprovider nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2102c-117">For example, setting the *Command Time out* property on a **Recordset** will not be visible to the underlying data provider.</span></span>

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

<span data-ttu-id="2102c-p106">Wenn Ihre Anwendung den Cursordienst erfordert, Sie jedoch dynamische Eigenschaften im zugrunde liegenden Anbieter festlegen müssen, tun Sie dies, bevor Sie den Cursordienst aufrufen. Einstellungen für Eigenschaften von Befehlsobjekten werden unabhängig von der Cursorplatzierung immer an den zugrundeliegenden Datenprovider weitergeleitet. Sie können daher auch jederzeit ein Befehlsobjekt zum Festlegen der Eigenschaften verwenden.</span><span class="sxs-lookup"><span data-stu-id="2102c-p106">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service. Command object property settings are always passed to the underlying data provider regardless of cursor location. Therefore, you can also use a command object to set the properties at any time.</span></span>

> [!NOTE]
> <span data-ttu-id="2102c-121">Die dynamische Eigenschaft DBPROP_SERVERDATAONINSERT wird vom Cursordienst nicht unterstützt, auch wenn sie vom zugrunde liegenden Datenprovider unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2102c-121">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2102c-122">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="2102c-122">Property Name</span></span></p></th>
<th><p><span data-ttu-id="2102c-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2102c-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2102c-124">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="2102c-124">Auto Recalc</span></span><br />
<span data-ttu-id="2102c-125">(DBPROP_ADC_AUTORECALC)</span><span class="sxs-lookup"><span data-stu-id="2102c-125">(DBPROP_ADC_AUTORECALC)</span></span></p></td>
<td><p><span data-ttu-id="2102c-p107">Bei Datensatzgruppen, die mit dem Datenstrukturierungsdienst erstellt wurden, gibt dieser Wert an, wie häufig berechnete und Aggregatspalten berechnet werden. Der Standardwert (Wert=1) bedeutet, dass eine Neuberechnung durchgeführt wird, wenn der Datenstrukturierungsdienst feststellt, dass sich die Werte geändert haben. Wenn der Wert 0 ist, werden die berechneten und Aggregatspalten nur berechnet, wenn die Hierarchie zum ersten Mal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2102c-p107">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated. The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed. If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2102c-129">Batch Size</span><span class="sxs-lookup"><span data-stu-id="2102c-129">Batch Size</span></span><br />
<span data-ttu-id="2102c-130">(DBPROP_ADC_BATCHSIZE)</span><span class="sxs-lookup"><span data-stu-id="2102c-130">(DBPROP_ADC_BATCHSIZE)</span></span></p></td>
<td><p><span data-ttu-id="2102c-p108">Gibt die Anzahl von Aktualisierungsanweisungen an, die vor dem Senden an die Datenquelle als Batch verarbeitet werden können. Je mehr Anweisungen in einem Batch, umso weniger Schleifen zum Datenspeicher sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2102c-p108">Indicates the number of update statements that can be batched before being sent to the data store. The more statements in a batch, the fewer round trips to the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2102c-133">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="2102c-133">Cache Child Rows</span></span><br />
<span data-ttu-id="2102c-134">(DBPROP_ADC_CACHECHILDROWS)</span><span class="sxs-lookup"><span data-stu-id="2102c-134">(DBPROP_ADC_CACHECHILDROWS)</span></span></p></td>
<td><p><span data-ttu-id="2102c-135">Bei Datensatzgruppen, die mit dem Datenstrukturierungsdienst erstellt wurden, gibt dieser Wert an, ob untergeordnete Datensatzgruppen zur späteren Verwendung in einem Cache gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2102c-135">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2102c-136">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="2102c-136">Cursor Engine Version</span></span><br />
<span data-ttu-id="2102c-137">(DBPROP_ADC_CEVER)</span><span class="sxs-lookup"><span data-stu-id="2102c-137">(DBPROP_ADC_CEVER)</span></span></p></td>
<td><p><span data-ttu-id="2102c-138">Gibt die Version des verwendeten Cursordiensts an.</span><span class="sxs-lookup"><span data-stu-id="2102c-138">Indicates the version of the Cursor Service being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2102c-139">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="2102c-139">Maintain Change Status</span></span><br />
<span data-ttu-id="2102c-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span><span class="sxs-lookup"><span data-stu-id="2102c-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span></span></p></td>
<td><p><span data-ttu-id="2102c-141">Gibt den Text des Befehls an, der zum erneuten Synchronisieren einer oder mehrerer Zeilen in einer Verknüpfung aus mehreren Tabellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2102c-141">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2102c-142"><a href="optimize-property-dynamic-ado.md">Optimieren der Leistung von</a></span><span class="sxs-lookup"><span data-stu-id="2102c-142"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="2102c-p109">Gibt an, ob ein Index erstellt werden soll. Wenn diese Eigenschaft auf <strong>True</strong> festgelegt ist, wird das temporäre Erstellen von Indizes zum Verbessern der Ausführung bestimmter Vorgänge zugelassen.</span><span class="sxs-lookup"><span data-stu-id="2102c-p109">Indicates whether an index should be created. When set to <strong>True</strong>, authorizes the temporary creation of indexes to improve the execution of certain operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2102c-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="2102c-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="2102c-p110">Gibt den Namen des <strong>Recordset</strong>-Objekts an. Darauf kann in aktuellen oder nachfolgenden Datenstrukturierungsbefehlen verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="2102c-p110">Indicates the name of the <strong>Recordset</strong>. May be referenced within the current, or subsequent, data shaping commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2102c-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="2102c-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="2102c-149">Gibt eine benutzerdefinierte Befehlszeichenfolge an, die von der <a href="resync-method-ado.md">Resync</a>-Methode verwendet wird, wenn die <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a>-Eigenschaft aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2102c-149">Indicates a custom command string that is used by the <a href="resync-method-ado.md">Resync</a> method when the <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> property is in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2102c-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="2102c-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="2102c-151">Gibt den Namen der Datenbank an, der die Tabelle enthält, auf die in der <strong>Unique Table</strong>-Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2102c-151">Indicates the name of the database containing the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2102c-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span><span class="sxs-lookup"><span data-stu-id="2102c-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span></span></p></td>
<td><p><span data-ttu-id="2102c-153">Gibt den Namen der Besitzers der Tabelle an, auf die in der <strong>Unique Table</strong>-Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2102c-153">Indicates the name of the owner of the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2102c-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span><span class="sxs-lookup"><span data-stu-id="2102c-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span></span></p></td>
<td><p><span data-ttu-id="2102c-155">Gibt den Namen der Tabelle in einem aus mehreren Tabellen erstellten <strong>Recordset</strong>-Objekt an, die durch Einfügungen, Aktualisierungen oder Löschvorgänge geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2102c-155">Indicates the name of the one table in a <strong>Recordset</strong> created from multiple tables that may be modified by insertions, updates, or deletions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2102c-156">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="2102c-156">Update Criteria</span></span><br />
<span data-ttu-id="2102c-157">(DBPROP_ADC_UPDATECRITERIA)</span><span class="sxs-lookup"><span data-stu-id="2102c-157">(DBPROP_ADC_UPDATECRITERIA)</span></span></p></td>
<td><p><span data-ttu-id="2102c-158">Gibt an, welche Felder in der <strong>WHERE</strong>-Klausel zum Behandeln von Konflikten bei einer Aktualisierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2102c-158">Indicates which fields in the <strong>WHERE</strong> clause are used to handle collisions occurring during an update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2102c-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span><span class="sxs-lookup"><span data-stu-id="2102c-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span></span></p></td>
<td><p><span data-ttu-id="2102c-160">Gibt an, ob die <strong>Resync</strong>-Methode nach der <a href="updatebatch-method-ado.md">UpdateBatch</a>-Methode (und dem jeweiligen Verhalten) implizit aufgerufen wird, wenn die <strong>Unique Table</strong>-Eigenschaft aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2102c-160">Indicates whether the <strong>Resync</strong> method is implicitly invoked after the <a href="updatebatch-method-ado.md">UpdateBatch</a> method (and its behavior), when the <strong>Unique Table</strong> property is in effect.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2102c-p111">Sie können auch eine dynamische Eigenschaft festlegen oder abrufen, indem Sie deren Namen als Index für die **Properties** -Auflistung angeben. Beispiel: Rufen Sie den aktuellen Wert der dynamischen Eigenschaft [Optimize](optimize-property-dynamic-ado.md) ab, und drucken Sie ihn. Legen Sie anschließend einen neuen Wert fest. Gehen Sie dazu wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="2102c-p111">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** collection. For example, get and print the current value of the [Optimize](optimize-property-dynamic-ado.md) dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a><span data-ttu-id="2102c-163">Verhalten integrierter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2102c-163">Built-in Property Behavior</span></span>

<span data-ttu-id="2102c-164">Der Microsoft Cursor Service für OLE DB hat auch Auswirkungen auf das Verhalten bestimmter integrierter Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2102c-164">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2102c-165">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="2102c-165">Property Name</span></span></p></th>
<th><p><span data-ttu-id="2102c-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2102c-166">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2102c-167"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="2102c-167"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="2102c-168">Ergänzt die für ein <strong>Recordset</strong>-Objekt verfügbaren Cursortypen.</span><span class="sxs-lookup"><span data-stu-id="2102c-168">Supplements the types of cursors that are available for a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2102c-169"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="2102c-169"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="2102c-p112">Ergänzt die für ein <strong>Recordset</strong>-Objekt verfügbaren Typen von Sperren. Ermöglicht Batchaktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="2102c-p112">Supplements the types of locks available for a <strong>Recordset</strong>. Enables batch updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2102c-172"><a href="sort-property-ado.md">Sort</a></span><span class="sxs-lookup"><span data-stu-id="2102c-172"><a href="sort-property-ado.md">Sort</a></span></span></p></td>
<td><p><span data-ttu-id="2102c-173">Gibt einen oder mehrere Feldnamen an, nach denen das <strong>Recordset</strong>-Objekt sortiert ist. Gibt außerdem an, ob die einzelnen Felder in auf- oder absteigender Folge sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="2102c-173">Specifies one or more field names that the <strong>Recordset</strong> is sorted on, and whether each field is sorted in ascending or descending order.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a><span data-ttu-id="2102c-174">Methodenverhalten</span><span class="sxs-lookup"><span data-stu-id="2102c-174">Method Behavior</span></span>

<span data-ttu-id="2102c-175">Der Microsoft Cursor Service für OLE DB ermöglicht oder beeinflusst das Verhalten der [Append](field-object-ado.md)-Methode des [Field](append-method-ado.md)-Objekts sowie der Methoden **Open**, [Resync](open-method-ado-recordset.md), [UpdateBatch](resync-method-ado.md) und [Save](updatebatch-method-ado.md) des [Recordset](save-method-ado.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2102c-175">The Cursor Service for OLE DB enables or affects the behavior of the [Field](field-object-ado.md) object's [Append](append-method-ado.md) method; and the **Recordset** object's [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [Save](save-method-ado.md) methods.</span></span>

