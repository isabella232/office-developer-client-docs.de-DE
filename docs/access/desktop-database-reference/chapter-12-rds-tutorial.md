---
title: 'Kapitel 12: Remote Data Service (RDS) Tutorial'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296479"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a><span data-ttu-id="6fbcd-102">Kapitel 12: Remote Data Service (RDS) Tutorial</span><span class="sxs-lookup"><span data-stu-id="6fbcd-102">Chapter 12: Remote Data Service (RDS) tutorial</span></span>

<span data-ttu-id="6fbcd-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fbcd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6fbcd-104">Dieses Lernprogramm zeigt, wie eine Datenquelle mit dem RDS-Programmiermodell abgefragt und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="6fbcd-105">Zunächst werden die Schritte beschrieben, die für diese Aufgabe nötig sind.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="6fbcd-106">Anschließend wird das Lernprogramm in Microsoft Visual Basic Scripting Edition und Microsoft Visual J++ mit ADO für Windows Foundation Classes (ADO/WFC) wiederholt.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="6fbcd-107">Aus zwei Gründen enthält dieses Lernprogramm Code in verschiedenen Sprachen:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="6fbcd-p102">Die Dokumentation für RDS setzt voraus, dass der Leser Visual Basic-Code verwendet. Dadurch eignet sich die Dokumentation besonders für Visual Basic-Programmierer, für Programmierer anderer Sprachen ist sie jedoch weniger praktisch.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="6fbcd-110">Wenn Sie bei einem bestimmten Feature von RDS unsicher sind und gewisse Sprachkenntnisse in einer anderen Sprache haben, finden Sie vielleicht eine Lösung zu Ihrer Frage, indem Sie nach demselben Feature in einer anderen Sprache suchen.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

<span data-ttu-id="6fbcd-p103">Dieses Lernprogramm basiert auf dem RDS-Programmiermodell. Die jeweiligen Schritte des Programmiermodells werden dabei einzeln vorgestellt. Darüber hinaus wird jeder Schritt durch einen Ausschnitt eines Visual Basic-Codes veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="6fbcd-p104">Das Codebeispiel wird ohne ausführliche Erläuterungen in weiteren Sprachen wiederholt. Jeder Schritt in einem Lernprogramm einer bestimmten Sprache ist mit dem entsprechenden Schritt im Programmiermodell und dem erläuternden Lernprogramm gekennzeichnet. Anhand der Schrittnummer finden Sie die Erläuterungen im Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="6fbcd-p105">Das RDS-Programmiermodell wird unten aufgeführt. Verwenden Sie es als Leitfaden, wenn Sie das Lernprogramm durchgehen.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

### <a name="rds-programming-model-with-objects"></a><span data-ttu-id="6fbcd-119">RDS-Programmiermodell mit Objekten</span><span class="sxs-lookup"><span data-stu-id="6fbcd-119">RDS programming model with objects</span></span>

- <span data-ttu-id="6fbcd-120">Geben Sie das auf dem Server aufzurufende Programm an, und ermitteln Sie eine Möglichkeit (Proxy), vom Client darauf zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-120">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="6fbcd-p106">Aufrufen des Serverprogramms. Übergeben von Parametern an das Serverprogramm, die die Datenquelle und den auszugebenden Befehl identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="6fbcd-p107">Das Serverprogramm ruft ein [Recordset](recordset-object-ado.md)-Objekt aus der Datenquelle ab, in der Regel unter Verwendung von ADO. Das **Recordset** -Objekt kann optional auf dem Server verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="6fbcd-125">Das Serverprogramm gibt das endgültige **Recordset** -Objekt an die Clientanwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-125">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="6fbcd-126">Auf dem Client wird das **Recordset**-Objekt optional in eine Form gebracht, die leicht von visuellen Steuerelementen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-126">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="6fbcd-127">Änderungen am **Recordset**-Objekt werden zurück an den Server gesendet und zur Aktualisierung der Datenquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-127">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

## <a name="step-1-specify-a-server-program"></a><span data-ttu-id="6fbcd-128">Schritt 1: Angeben eines Serverprogramms</span><span class="sxs-lookup"><span data-stu-id="6fbcd-128">Step 1: Specify a server program</span></span>

<span data-ttu-id="6fbcd-p108">Verwenden Sie ganz allgemein die [CreateObject](createobject-method-rds.md)-Methode des [RDS.DataSpace](dataspace-object-rds.md)-Objekts zum Angeben des Standardserverprogramms, [RDSServer.DataFactory](datafactory-object-rdsserver.md), oder Ihres eigenen benutzerdefinierten Serverprogramms (Geschäftsobjekt). Ein Serverprogramm wird auf dem Server instanziiert, und ein Verweis auf das Serverprogramm bzw. den *Proxy* wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p108">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object). A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="6fbcd-131">In diesem Lernprogramm wird das Standardserverprogramm verwendet:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-131">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a><span data-ttu-id="6fbcd-132">Schritt 2: Aufrufen des Serverprogramms</span><span class="sxs-lookup"><span data-stu-id="6fbcd-132">Step 2: Invoke the server program</span></span> 

<span data-ttu-id="6fbcd-p109">Wenn Sie auf dem Client*proxy* eine Methode aufrufen, wird die Methode vom tatsächlichen Programm auf dem Server ausgeführt. In diesem Schritt führen Sie eine Abfrage auf dem Server durch.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p109">When you invoke a method on the client *proxy*, the actual program on the server executes the method. In this step, you'll execute a query on the server.</span></span>

### <a name="part-a"></a><span data-ttu-id="6fbcd-135">Teil A </span><span class="sxs-lookup"><span data-stu-id="6fbcd-135">Part A</span></span>

<span data-ttu-id="6fbcd-136">Wenn Sie in diesem Lernprogramm nicht [RDSServer.DataFactory](datafactory-object-rdsserver.md) verwenden würden, wäre die Verwendung des [RDS.DataControl](datacontrol-object-rds.md)-Objekts bei diesem Schritt am praktischsten.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-136">If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="6fbcd-137">Das **RDS.DataControl**-Objekt verbindet den vorherigen Schritt des Erstellens eines Proxys mit diesem Schritt des Erstellens einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-137">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

1. <span data-ttu-id="6fbcd-138">Legen Sie **RDS fest. DataControl** -Objekt [Server](server-property-rds.md) Eigenschaft, um anzugeben, wo das Server Programm instanziiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-138">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated.</span></span>

2. <span data-ttu-id="6fbcd-139">Legen Sie die [Connect](connect-property-rds.md) -Eigenschaft fest, um die Verbindungszeichenfolge für den Zugriff auf die Datenquelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-139">Set the [Connect](connect-property-rds.md) property to specify the connect string to access the data source.</span></span>

3. <span data-ttu-id="6fbcd-140">Legen Sie die [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) -Eigenschaft fest, um den Abfragebefehlstext anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-140">Set the [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property to specify the query command text.</span></span> 

4. <span data-ttu-id="6fbcd-141">Geben Sie die [Refresh](refresh-method-rds.md) -Methode an, damit das Serverprogramm eine Verbindung mit der Datenquelle herstellen, von der Abfrage angegebene Zeilen abrufen und ein **Recordset** -Objekt an den Client zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-141">Issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="6fbcd-142">In diesem Lernprogramm wird zwar kein **RDS.DataControl** -Objekt verwendet, es würde jedoch folgendermaßen auftreten:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-142">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

<span data-ttu-id="6fbcd-143">In diesem Lernprogramm wird RDS auch nicht mit ADO-Objekten aufgerufen, was folgendermaßen aussehen würde:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-143">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a><span data-ttu-id="6fbcd-144">Teil B </span><span class="sxs-lookup"><span data-stu-id="6fbcd-144">Part B</span></span>

<span data-ttu-id="6fbcd-145">Im Allgemeinen wird dieser Schritt ausgeführt, indem die [Query](query-method-rds.md)-Methode des **RDSServer.DataFactory**-Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-145">The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="6fbcd-146">In diese Methode wird anhand einer Verbindungszeichenfolge eine Verbindung mit der Datenquelle hergestellt, und mit einem Befehlstext werden die Zeilen angegeben, die aus der Datenquelle zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-146">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="6fbcd-147">In diesem Lernprogramm wird die **Query** -Methode des **DataFactory** -Objekts verwendet:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-147">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a><span data-ttu-id="6fbcd-148">Schritt 3: Server Ruft ein Recordset-Objekt ab</span><span class="sxs-lookup"><span data-stu-id="6fbcd-148">Step 3: Server obtains a Recordset</span></span> 

<span data-ttu-id="6fbcd-p112">Das Serverprogramm verwendet die Verbindungszeichenfolge und den Befehlstext, um die gewünschten Zeilen in der Datenquelle abzufragen. In der Regel wird ADO zum Abrufen dieses **Recordset** -Objekts verwendet, obwohl auch andere Datenzugriffsschnittstellen verwendet werden könnten (z. B. OLE DB).</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p112">The server program uses the connect string and command text to query the data source for the desired rows. ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="6fbcd-151">Ein benutzerdefiniertes Serverprogramm kann folgendermaßen aussehen:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-151">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="6fbcd-152">Schritt 4: Server gibt das Recordset-Objekt zurück</span><span class="sxs-lookup"><span data-stu-id="6fbcd-152">Step 4: Server returns the Recordset</span></span> 

<span data-ttu-id="6fbcd-p113">RDS konvertiert das abgerufene **Recordset**-Objekt in eine Form, die zurück an den Client gesendet werden kann (d. h. das **Recordset**-Objekt wird *gemarshallt*). In welcher Form das Objekt genau konvertiert und gesendet wird, hängt davon ab, ob sich der Server im Internet, dem Intranet oder einem LAN befindet oder ob es sich um eine DLL handelt. Diese Details ist jedoch nicht wichtig. Entscheidend ist, dass RDS das **Recordset**-Objekt zurück an den Client sendet.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p113">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**). The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library. However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="6fbcd-156">Auf dem Client wird ein **Recordset**-Objekt an eine lokale Variable zurückgegeben und dieser Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-156">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a><span data-ttu-id="6fbcd-157">Schritt 5: DataControl ist nutzbar</span><span class="sxs-lookup"><span data-stu-id="6fbcd-157">Step 5: DataControl is made usable</span></span> 

<span data-ttu-id="6fbcd-p114">Das zurückgegebene **Recordset**-Objekt kann verwendet werden. Sie können es wie jedes andere **Recordset**-Objekt überprüfen, bearbeiten oder darin navigieren. Die Bearbeitungsmöglichkeiten des **Recordset**-Objekts hängen von der Umgebung ab. Visual Basic und Visual C++ besitzen visuelle Steuerelemente, die ein **Recordset**-Objekt direkt oder indirekt mithilfe eines aktivierenden Datensteuerelements verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p114">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="6fbcd-162">Wenn Sie beispielsweise eine Webseite in Internet Explorer anzeigen, möchten Sie möglicherweise die Daten des **Recordset** -Objekts in einem visuellen SteuerelementAnzeigen.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-162">For example, if you are displaying a webpage in Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="6fbcd-163">Visuelle Steuerelemente auf einer Webseite können nicht direkt auf ein **Recordset** -Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-163">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="6fbcd-164">Der Zugriff auf das **Recordset** ist jedoch über das [RDS.DataControl](datacontrol-object-rds.md)-Objekt möglich.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-164">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="6fbcd-165">Das **RDS.DataControl**-Objekt kann von einem visuellen Steuerelement verwendet werden, wenn seine [SourceRecordset](recordset-sourcerecordset-properties-rds.md)-Eigenschaft auf das **Recordset**-Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-165">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="6fbcd-166">Der **DATASRC**-Parameter eines visuellen Steuerelements muss auf **RDS.DataControl** und seine **DATAFLD**-Eigenschaft auf ein **Recordset**-Objektfeld (Spalte) festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-166">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="6fbcd-167">In diesem Lernprogramm legen Sie die **SourceRecordset**-Eigenschaft fest:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-167">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a><span data-ttu-id="6fbcd-168">Schritt 6: Änderungen werden an den Server gesendet</span><span class="sxs-lookup"><span data-stu-id="6fbcd-168">Step 6: Changes are sent to the server</span></span>

<span data-ttu-id="6fbcd-169">Beim Bearbeiten eines **Recordset** -Objekts können alle Änderungen (d. h. hinzugefügte, geänderte oder gelöschte Zeilen) zurück an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-169">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="6fbcd-170">[!HINWEIS] Das Standardverhalten von RDS kann implizit mit ADO-Objekten und dem Microsoft OLE DB-Anbieter für Remoting aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-170">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="6fbcd-171">Abfragen können **Recordsets**zurückgeben, und beArbeitete **Recordsets** können die Datenquelle aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-171">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="6fbcd-172">In diesem Lernprogramm wird RDS nicht mit ADO-Objekten aufgerufen, was folgendermaßen aussehen würde:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-172">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a><span data-ttu-id="6fbcd-173">Teil A </span><span class="sxs-lookup"><span data-stu-id="6fbcd-173">Part A</span></span>

<span data-ttu-id="6fbcd-174">Gehen Sie in diesem Fall davon aus, dass Sie nur das [RDS.DataControl](datacontrol-object-rds.md)-Objekt verwendet haben und dass ein **Recordset**-Objekt nun mit dem **RDS.DataControl**-Objekt verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-174">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="6fbcd-175">Die Datenquelle wird durch die [SubmitChanges](submitchanges-method-rds.md)-Methode mit allen Änderungen am **Recordset**-Objekt aktualisiert, wenn die Eigenschaften [Server](server-property-rds.md) und [Connect](connect-property-rds.md) noch festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-175">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

### <a name="part-b"></a><span data-ttu-id="6fbcd-176">Teil B </span><span class="sxs-lookup"><span data-stu-id="6fbcd-176">Part B</span></span>

<span data-ttu-id="6fbcd-177">Sie können alternativ den Server mit dem [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt aktualisieren und eine Verbindung sowie ein **Recordset**-Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-177">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```


## <a name="appendix-a-rds-tutorial-vbscript"></a><span data-ttu-id="6fbcd-178">Anhang A: RDS-Lernprogramm (VBScript)</span><span class="sxs-lookup"><span data-stu-id="6fbcd-178">Appendix A: RDS tutorial (VBScript)</span></span>

<span data-ttu-id="6fbcd-179">Dies ist das RDS-Lernprogramm, geschrieben in Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-179">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="6fbcd-180">Eine Beschreibung des Zwecks dieses Lernprogramms finden Sie in der Einführung zu diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-180">For a description of the purpose of this tutorial, see the introduction to this topic.</span></span>

<span data-ttu-id="6fbcd-181">In diesem Lernprogramm wird [RDS. DataControl](datacontrol-object-rds.md) und [RDS. DataSpace](dataspace-object-rds.md) werden zur Entwurfszeit erstellt; Das heißt, Sie werden mit Objekttags definiert.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-181">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="6fbcd-182">Alternativ können diese Objekte auch zur Laufzeit mit der **Server.CreateObject** -Methode erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-182">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="6fbcd-183">Sie können das **RDS.DataControl** -Objekt beispielsweise folgendermaßen erstellen:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-183">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

### <a name="step-1-specify-a-server-program"></a><span data-ttu-id="6fbcd-184">Schritt 1: Angeben eines Serverprogramms</span><span class="sxs-lookup"><span data-stu-id="6fbcd-184">Step 1: Specify a server program</span></span>

<span data-ttu-id="6fbcd-185">VBScript kann den Namen des IIS-Webservers ermitteln, auf dem er läuft, indem Sie auf die für Active Server Pages verfügbare VBScript-Methode **Request. ServerVariablesund** zugreifen:</span><span class="sxs-lookup"><span data-stu-id="6fbcd-185">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="6fbcd-186">Verwenden Sie jedoch für dieses Lernprogramm den imaginären Server "yourServer".</span><span class="sxs-lookup"><span data-stu-id="6fbcd-186">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="6fbcd-p120">Pay attention to the data type of **ByRef** arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p120">Pay attention to the data type of **ByRef** arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="6fbcd-191">Schritt 2, Teil A: Aufrufen des Serverprogramms mit RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="6fbcd-191">Step 2, Part A: Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="6fbcd-192">Das folgende Beispiel dient lediglich zur Veranschaulichung, dass das Standardverhalten des **RDS.DataControl** -Objekts im Ausführen der angegebenen Abfrage besteht.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-192">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

<span data-ttu-id="6fbcd-193">Fahren Sie mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-193">Skip to the following step.</span></span>

### <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="6fbcd-194">Schritt 4: Server gibt das Recordset-Objekt zurück</span><span class="sxs-lookup"><span data-stu-id="6fbcd-194">Step 4: Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="6fbcd-195">Schritt 5: DataControl wird von visuellen Steuerelementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-195">Step 5: DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="6fbcd-196">Schritt 6, Teil A: Änderungen werden mit RDS an den Server gesendet. DataControl</span><span class="sxs-lookup"><span data-stu-id="6fbcd-196">Step 6, Part A: Changes are sent to the server with RDS.DataControl</span></span>

<span data-ttu-id="6fbcd-197">Das folgende Beispiel dient lediglich zur Veranschaulichung, wie das **RDS.DataControl** -Objekt Aktualisierungen ausführt.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-197">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="6fbcd-198">Schritt 6, Teil B: Änderungen werden mit RDSServer. dataFactory an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-198">Step 6, Part B: Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a><span data-ttu-id="6fbcd-199">Anhang B: RDS-Lernprogramm (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="6fbcd-199">Appendix B: RDS tutorial (Visual J++)</span></span>

<span data-ttu-id="6fbcd-p121">ADO/WFC entspricht insofern, als das [RDS.DataControl](datacontrol-object-rds.md)-Objekt nicht implementiert wird, nicht vollständig dem RDS-Objektmodell. ADO/WFC implementiert lediglich die clientseitige Klasse [RDS.DataSpace](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p121">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object. ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="6fbcd-p122">Die **DataSpace** -Klasse implementiert eine [CreateObject](createobject-method-rds.md)-Methode, die wiederum ein [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax)-Objekt zurückgibt. Die **DataSpace** -Klasse implementiert auch die [InternetTimeout](internettimeout-property-rds.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p122">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) object. The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="6fbcd-204">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-204">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



