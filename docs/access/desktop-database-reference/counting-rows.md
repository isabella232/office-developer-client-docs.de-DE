---
title: Zählen von Zeilen (Access PC-Datenbank-Referenz)
TOCTitle: Counting rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39468086e7c78a89b13b6021c7f07853c487c6e5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945306"
---
# <a name="counting-rows"></a><span data-ttu-id="01649-102">Zählen von Zeilen</span><span class="sxs-lookup"><span data-stu-id="01649-102">Counting rows</span></span>


<span data-ttu-id="01649-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="01649-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01649-p101">Die **RecordCount** -Eigenschaft gibt einen Wert vom Datentyp **Long** für die Anzahl von Datensätzen im **Recordset** -Objekt zurück. Mithilfe der **RecordCount** -Eigenschaft stellen Sie die Anzahl der Datensätze im **Recordset** -Objekt fest. Diese Eigenschaft gibt -1 zurück, wenn ADO die Anzahl von Datensätzen nicht bestimmen kann, oder wenn **RecordCount** vom Anbieter oder Cursortyp nicht unterstützt wird. Ein Fehler wird gemeldet, wenn die **RecordCount** -Eigenschaft für ein geschlossenes **Recordset** -Objekt gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="01649-p101">The **RecordCount** property returns a **Long** value that indicates the number of records in the **Recordset**. Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="01649-p102">Die **RecordCount** -Eigenschaft hängt von der Funktionalität des Anbieters und vom Cursortyp ab. Mit der **RecordCount** -Eigenschaft wird -1 für einen Vorwärtscursor, die tatsächliche Anzahl für einen statischen Cursor oder einen Keysetcursor, und je nach Datenquelle -1 oder die tatsächliche Anzahl für einen dynamischen Cursor zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01649-p102">The **RecordCount** property depends on the capabilities of the provider and the type of cursor. The **RecordCount** property will return -1 for a forward-only cursor, the actual count for a static or keyset cursor, and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

<span data-ttu-id="01649-110">Im Beispiel **Recordset** eingeführt in [Untersuchen von Daten](chapter-3-examining-data.md) würde – 1 zurück, da ein Vorwärtscursor geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="01649-110">The sample **Recordset** introduced in [Examining Data](chapter-3-examining-data.md) would return –1 because a forward-only cursor was opened.</span></span> <span data-ttu-id="01649-111">Für die Verwendung der **RecordCount** -Eigenschaft müssten Sie das **Recordset** -Objekt mit einem leistungsfähigeren Cursor (statischer Cursor oder Keysetcursor) öffnen.</span><span class="sxs-lookup"><span data-stu-id="01649-111">In order to use the **RecordCount** property, you would need to open the **Recordset** with a more sophisticated cursor (static or keyset).</span></span>

<span data-ttu-id="01649-p104">Es kann vorkommen, dass der Anbieter oder Cursor den Wert für die **RecordCount** -Eigenschaft nur bereitstellen kann, wenn zuerst alle Datensätze von der Datenquelle abgerufen werden. Rufen Sie die **MoveLast** -Methode des **Recordset** -Objekts vor **RecordCount** auf, um diese Art von Abrufen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="01649-p104">In certain cases, your provider or cursor might be unable to provide the **RecordCount** value without first fetching all records from the data source. To force this type of fetch, call the **Recordset** **MoveLast** method before calling **RecordCount**.</span></span>

<span data-ttu-id="01649-114">Angenommen, Sie müssten die Codezeile, mit der die **Open** -Methode des **Recordset** -Objekts aufgerufen wird, durch folgenden Code ersetzen:</span><span class="sxs-lookup"><span data-stu-id="01649-114">If you were to replace the line of code that calls the **Recordset** **Open** method with the following:</span></span>

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="01649-p105">In diesem Fall könnten Sie die **RecordCount** -Eigenschaft verwenden, weil [RecordCount](microsoft-ole-db-provider-for-sql-server.md) von statischen Cursorn mit dem **Microsoft OLE DB-Anbieter für SQL Server** unterstützt werden. Beispielsweise würde der folgende Code die von dem Befehl zurückgegebene Anzahl von Datensätzen im Debugfenster ausgeben, vorausgesetzt die **RecordCount** -Eigenschaft wird vom Cursor unterstützt:</span><span class="sxs-lookup"><span data-stu-id="01649-p105">you would be able to use the **RecordCount** property because static cursors with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) support **RecordCount**. For example, the following code would print out the number of records returned by the command to the debug window, assuming the cursor supports the **RecordCount** property:</span></span>

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

<span data-ttu-id="01649-117">Von da an sollten diese leistungsfähigeren (aber teureren) Cursor- und Sperrtypeinstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01649-117">From this point forward, assume that these more capable (but more expensive) cursor and lock type settings are used.</span></span>

