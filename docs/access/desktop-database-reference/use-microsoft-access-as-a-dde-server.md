---
title: Verwenden von Microsoft Access als DDE-Server
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access unterstützt Dynamic Data Exchange (DDE) als Ziel-(Client-) Anwendung oder als Quellanwendung (Server).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0750bdce0e1cda383c48f9c16e62e00997fdfb0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313391"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="8ad22-103">Verwenden von Microsoft Access als DDE-Server</span><span class="sxs-lookup"><span data-stu-id="8ad22-103">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="8ad22-104">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ad22-104">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="8ad22-105">Microsoft Access unterstützt Dynamic Data Exchange (DDE) als Ziel-(Client-) Anwendung oder als Quellanwendung (Server).</span><span class="sxs-lookup"><span data-stu-id="8ad22-105">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span> <span data-ttu-id="8ad22-106">Beispielsweise kann eine Anwendung wie Microsoft Word, die als Client fungiert, Daten über DDE aus einer Microsoft Access-Datenbank anfordern, die als Server fungiert.</span><span class="sxs-lookup"><span data-stu-id="8ad22-106">For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="8ad22-107">Wenn Sie Microsoft Access-Objekte aus einer anderen Anwendung bearbeiten müssen, sollten Sie die Automatisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ad22-107">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="8ad22-108">Eine DDE-Unterhaltung zwischen einem Client und einem Server wird zu einem bestimmten Thema hergestellt.</span><span class="sxs-lookup"><span data-stu-id="8ad22-108">A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="8ad22-109">Bei einem Thema kann es sich entweder um eine Datendatei im von der Serveranwendung unterstützten Format oder um das System Thema handeln, das Informationen zur Serveranwendung selbst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ad22-109">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="8ad22-110">Nachdem eine Unterhaltung zu einem bestimmten Thema begonnen hat, kann nur ein diesem Thema zugeordnetes Datenelement übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="8ad22-110">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="8ad22-111">Angenommen, Sie führen Microsoft Word aus und möchten Daten aus einer bestimmten Microsoft Access-Datenbank in ein Dokument einfügen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-111">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document.</span></span> <span data-ttu-id="8ad22-112">Sie beginnen eine DDE-Unterhaltung mit Microsoft Access, indem Sie einen DDE-Kanal mit der **DDEInitiate** -Funktion öffnen und den Namen der Datenbankdatei als Thema angeben.</span><span class="sxs-lookup"><span data-stu-id="8ad22-112">You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic.</span></span> <span data-ttu-id="8ad22-113">Sie können dann Daten aus dieser Datenbank über diesen Kanal zu Microsoft Word übertragen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-113">You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="8ad22-114">Als DDE-Server unterstützt Microsoft Access die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="8ad22-114">As a DDE server, Microsoft Access supports the following topics:</span></span>

- <span data-ttu-id="8ad22-115">Das Thema System</span><span class="sxs-lookup"><span data-stu-id="8ad22-115">The System topic</span></span>

- <span data-ttu-id="8ad22-116">Der Name einer Datenbank (*Daten Bank* Thema)</span><span class="sxs-lookup"><span data-stu-id="8ad22-116">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="8ad22-117">Der Name einer Tabelle (TableName-Thema)\*\*</span><span class="sxs-lookup"><span data-stu-id="8ad22-117">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="8ad22-118">Der Name einer Abfrage (Thema\*\* "QueryName")</span><span class="sxs-lookup"><span data-stu-id="8ad22-118">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="8ad22-119">Eine Microsoft Access-SQL-Zeichenfolge (*SqlString* -Thema)</span><span class="sxs-lookup"><span data-stu-id="8ad22-119">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="8ad22-120">Nachdem Sie eine DDE-Unterhaltung erstellt haben, können Sie die **DDEExecute** -Anweisung verwenden, um einen Befehl vom Client an die Serveranwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="8ad22-120">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="8ad22-121">Bei Verwendung als DDE-Server erkennt Microsoft Access die folgenden als gültigen Befehl:</span><span class="sxs-lookup"><span data-stu-id="8ad22-121">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="8ad22-122">Der Name eines Makros in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8ad22-122">The name of a macro in the current database.</span></span>

- <span data-ttu-id="8ad22-123">Jede Aktion, die Sie in Visual Basic ausführen können, indem Sie eine der Methoden des **DoCmd** -Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ad22-123">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="8ad22-124">Die openDatabase-und SchließenDatenbank-Aktionen, die nur für DDE-Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ad22-124">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations.</span></span> <span data-ttu-id="8ad22-125">(Ein Beispiel für die Verwendung dieser Aktionen finden Sie im Beispiel weiter unten in diesem Thema.)</span><span class="sxs-lookup"><span data-stu-id="8ad22-125">(For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="8ad22-126">Wenn Sie eine Makroaktion als **DDEExecute** -Anweisung angeben, folgen die Aktion und alle Argumente der **DoCmd** -Objektsyntax und müssen in eckige Klammern ([]) eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8ad22-126">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]).</span></span> <span data-ttu-id="8ad22-127">Anwendungen, die DDE unterstützen, erkennen jedoch keine systeminternen Konstanten in DDE-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-127">However, applications that support DDE don't recognize intrinsic constants in DDE operations.</span></span> <span data-ttu-id="8ad22-128">Auch Zeichenfolgenargumente müssen in Anführungszeichen ("") eingeschlossen werden, wenn die Zeichenfolge ein Komma enthält.</span><span class="sxs-lookup"><span data-stu-id="8ad22-128">Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma.</span></span> <span data-ttu-id="8ad22-129">Andernfalls sind keine Anführungszeichen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ad22-129">Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="8ad22-130">Die Clientanwendung kann die **DDERequest** -Funktion verwenden, um Text Daten aus der Serveranwendung über einen geöffneten DDE-Kanal anzufordern.</span><span class="sxs-lookup"><span data-stu-id="8ad22-130">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="8ad22-131">Oder der Client kann die **DDEPoke** -Anweisung verwenden, um Daten an die Serveranwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="8ad22-131">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="8ad22-132">Nach Abschluss der Datenübertragung kann der Client die **DDETerminate** -Anweisung verwenden, um den DDE-Kanal zu schließen, oder die **DDETerminateAll** -Anweisung, um alle geöffneten Kanäle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-132">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="8ad22-133">Wenn die Clientanwendung den Empfang von Daten über einen DDE-Kanal abgeschlossen hat, sollte dieser Kanal geschlossen werden, um Speicherressourcen zu sparen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-133">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>

<span data-ttu-id="8ad22-134">Das folgende Beispiel veranschaulicht, wie Sie eine Microsoft Word-Prozedur mit Visual Basic erstellen, die Microsoft Access als DDE-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ad22-134">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server.</span></span> <span data-ttu-id="8ad22-135">(Damit dieses Beispiel funktioniert, muss Microsoft Access ausgeführt werden.)</span><span class="sxs-lookup"><span data-stu-id="8ad22-135">(For this example to work, Microsoft Access must be running.)</span></span>

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<br/>

<span data-ttu-id="8ad22-136">Die folgenden Abschnitte enthalten Informationen zu den gültigen DDE-Themen, die von Microsoft Access unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8ad22-136">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="8ad22-137">Das Thema System</span><span class="sxs-lookup"><span data-stu-id="8ad22-137">The System topic</span></span>

<span data-ttu-id="8ad22-138">Das Thema System ist ein Standardthema für alle Microsoft Windows-basierten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-138">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="8ad22-139">Sie liefert Informationen zu den anderen von der Anwendung unterstützten Themen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-139">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="8ad22-140">Um auf diese Informationen zuzugreifen, muss der Code zunächst die **DDEInitiate** -Funktion mit dem *Thema* -Argument aufrufen und dann die **DDERequest** -Anweisung mit einem der folgenden für das Argument *Item* bereitgestellt ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-140">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ad22-141">Element</span><span class="sxs-lookup"><span data-stu-id="8ad22-141">Item</span></span></p></th>
<th><p><span data-ttu-id="8ad22-142">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8ad22-142">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-143">SysItems</span><span class="sxs-lookup"><span data-stu-id="8ad22-143">SysItems</span></span></p></td>
<td><p><span data-ttu-id="8ad22-144">Eine Liste der vom Thema "System" unterstützten Elemente in Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8ad22-144">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-145">Formats</span><span class="sxs-lookup"><span data-stu-id="8ad22-145">Formats</span></span></p></td>
<td><p><span data-ttu-id="8ad22-146">Eine Liste der Formate, die Microsoft Access in die Zwischenablage kopieren kann.</span><span class="sxs-lookup"><span data-stu-id="8ad22-146">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-147">Status</span><span class="sxs-lookup"><span data-stu-id="8ad22-147">Status</span></span></p></td>
<td><p><span data-ttu-id="8ad22-148">&quot;Besetzt&quot; oder &quot;bereit&quot;.</span><span class="sxs-lookup"><span data-stu-id="8ad22-148">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-149">Themen</span><span class="sxs-lookup"><span data-stu-id="8ad22-149">Topics</span></span></p></td>
<td><p><span data-ttu-id="8ad22-150">Eine Liste aller geöffneten Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="8ad22-150">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="8ad22-151">Das folgende Beispiel veranschaulicht die Verwendung der **DDEInitiate** -und **DDERequest** -Funktionen mit dem Thema System:</span><span class="sxs-lookup"><span data-stu-id="8ad22-151">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a><span data-ttu-id="8ad22-152">Das Daten Bank Thema</span><span class="sxs-lookup"><span data-stu-id="8ad22-152">The database topic</span></span>

<span data-ttu-id="8ad22-153">Das Thema *Datenbank* ist der Dateiname einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8ad22-153">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="8ad22-154">Sie können entweder nur den Basisnamen (Northwind) oder den Pfad und die MDB-Erweiterung (C:\\Access\\Samples\\Northwind. mdb) eingeben.</span><span class="sxs-lookup"><span data-stu-id="8ad22-154">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="8ad22-155">Nachdem Sie eine DDE-Unterhaltung mit der Datenbank gestartet haben, können Sie eine Liste der Objekte in dieser Datenbank anfordern.</span><span class="sxs-lookup"><span data-stu-id="8ad22-155">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

> [!NOTE]
> <span data-ttu-id="8ad22-156">Sie können DDE nicht verwenden, um die Microsoft Access-Arbeitsgruppen-Informationsdatei abzufragen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-156">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>

<span data-ttu-id="8ad22-157">Das *Daten Bank* Thema unterstützt die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="8ad22-157">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ad22-158">Element</span><span class="sxs-lookup"><span data-stu-id="8ad22-158">Item</span></span></p></th>
<th><p><span data-ttu-id="8ad22-159">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8ad22-159">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-160">TableList</span><span class="sxs-lookup"><span data-stu-id="8ad22-160">TableList</span></span></p></td>
<td><p><span data-ttu-id="8ad22-161">Eine Liste der Tabellen</span><span class="sxs-lookup"><span data-stu-id="8ad22-161">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-162">Abfragelist</span><span class="sxs-lookup"><span data-stu-id="8ad22-162">QueryList</span></span></p></td>
<td><p><span data-ttu-id="8ad22-163">Eine Liste von Abfragen</span><span class="sxs-lookup"><span data-stu-id="8ad22-163">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-164">Formularlist</span><span class="sxs-lookup"><span data-stu-id="8ad22-164">FormList</span></span></p></td>
<td><p><span data-ttu-id="8ad22-165">Eine Liste der Formulare</span><span class="sxs-lookup"><span data-stu-id="8ad22-165">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-166">ReportList</span><span class="sxs-lookup"><span data-stu-id="8ad22-166">ReportList</span></span></p></td>
<td><p><span data-ttu-id="8ad22-167">Eine Liste der Berichte</span><span class="sxs-lookup"><span data-stu-id="8ad22-167">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-168">Makroliste</span><span class="sxs-lookup"><span data-stu-id="8ad22-168">MacroList</span></span></p></td>
<td><p><span data-ttu-id="8ad22-169">Eine Liste von Makros</span><span class="sxs-lookup"><span data-stu-id="8ad22-169">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-170">Katalogisiert</span><span class="sxs-lookup"><span data-stu-id="8ad22-170">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="8ad22-171">Eine Liste der Module</span><span class="sxs-lookup"><span data-stu-id="8ad22-171">A list of modules</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-172">ViewList</span><span class="sxs-lookup"><span data-stu-id="8ad22-172">ViewList</span></span></p></td>
<td><p><span data-ttu-id="8ad22-173">Eine Liste der Ansichten</span><span class="sxs-lookup"><span data-stu-id="8ad22-173">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-174">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="8ad22-174">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="8ad22-175">Eine Liste der gespeicherten Prozeduren</span><span class="sxs-lookup"><span data-stu-id="8ad22-175">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-176">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="8ad22-176">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="8ad22-177">Eine Liste von Datenbankdiagrammen</span><span class="sxs-lookup"><span data-stu-id="8ad22-177">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="8ad22-178">Das folgende Beispiel zeigt, wie Sie das Employees-Formular in der Northwind-Beispieldatenbank aus einer Visual Basic-Prozedur öffnen können:</span><span class="sxs-lookup"><span data-stu-id="8ad22-178">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a><span data-ttu-id="8ad22-179">Das Thema "Tabelle"</span><span class="sxs-lookup"><span data-stu-id="8ad22-179">The TABLE topic</span></span>

<span data-ttu-id="8ad22-180">In diesen Themen wird die folgende Syntax verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ad22-180">These topics use the following syntax:</span></span>

<span data-ttu-id="8ad22-181">_DatabaseName_ ; **Tabelle** _TableName_</span><span class="sxs-lookup"><span data-stu-id="8ad22-181">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="8ad22-182">_DatabaseName_ ; **Abfrage** _Abfragename_</span><span class="sxs-lookup"><span data-stu-id="8ad22-182">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="8ad22-183">_DatabaseName_ ; **SQL** [ _SqlString_ ]</span><span class="sxs-lookup"><span data-stu-id="8ad22-183">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ad22-184">Teil</span><span class="sxs-lookup"><span data-stu-id="8ad22-184">Part</span></span></p></th>
<th><p><span data-ttu-id="8ad22-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ad22-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-186"><em>DatabaseName</em></span><span class="sxs-lookup"><span data-stu-id="8ad22-186"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="8ad22-187">Der Name der Datenbank, in der sich die Tabelle oder Abfrage befindet oder für die die SQL-Anweisung gilt, gefolgt von einem Semikolon (;).</span><span class="sxs-lookup"><span data-stu-id="8ad22-187">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;).</span></span> <span data-ttu-id="8ad22-188">Bei dem Datenbanknamen kann es sich um den Basisnamen (Northwind) oder den vollständigen Pfad und die MDB-Erweiterung (C:\Access\Samples\Northwind.mdb) handeln.</span><span class="sxs-lookup"><span data-stu-id="8ad22-188">The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-189"><em>TableName</em></span><span class="sxs-lookup"><span data-stu-id="8ad22-189"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="8ad22-190">Der Name einer vorhandenen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8ad22-190">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-191"><em>Abfragename</em></span><span class="sxs-lookup"><span data-stu-id="8ad22-191"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="8ad22-192">Der Name einer vorhandenen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8ad22-192">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-193"><em>SqlString</em></span><span class="sxs-lookup"><span data-stu-id="8ad22-193"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="8ad22-194">Eine gültige SQL-Anweisung bis zu 256 Zeichen lang, endend mit einem Semikolon.</span><span class="sxs-lookup"><span data-stu-id="8ad22-194">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="8ad22-195">Wenn Sie mehr als 256 Zeichen austauschen möchten, lassen Sie dieses Argument aus, und verwenden Sie stattdessen aufeinanderfolgende <strong>DDEPoke</strong> -Anweisungen, um eine SQL-Anweisung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-195">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="8ad22-196">Im folgenden Visual Basic-Code wird beispielsweise die <strong>DDEPoke</strong> -Anweisung verwendet, um eine SQL-Anweisung zu erstellen und dann die Ergebnisse der Abfrage anzufordern.</span><span class="sxs-lookup"><span data-stu-id="8ad22-196">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="8ad22-197">In der folgenden Tabelle sind die gültigen Elemente für die \*\* Tabellen TableName-, Query *QueryName*-und SQL *SqlString* -Themen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ad22-197">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ad22-198">Element</span><span class="sxs-lookup"><span data-stu-id="8ad22-198">Item</span></span></p></th>
<th><p><span data-ttu-id="8ad22-199">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8ad22-199">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-200">Alle</span><span class="sxs-lookup"><span data-stu-id="8ad22-200">All</span></span></p></td>
<td><p><span data-ttu-id="8ad22-201">Alle Daten in der Tabelle, einschließlich Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-201">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-202">Daten</span><span class="sxs-lookup"><span data-stu-id="8ad22-202">Data</span></span></p></td>
<td><p><span data-ttu-id="8ad22-203">Alle Datenzeilen ohne Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-203">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-204">FieldNames</span><span class="sxs-lookup"><span data-stu-id="8ad22-204">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="8ad22-205">Eine einzeilige Liste von Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="8ad22-205">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-206">FieldNames T</span><span class="sxs-lookup"><span data-stu-id="8ad22-206">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="8ad22-207">Eine zweireihige Liste von Feldnamen (erste Zeile) und deren Datentypen (zweite Zeile).</span><span class="sxs-lookup"><span data-stu-id="8ad22-207">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="8ad22-208">Dies sind die zurückgegebenen Werte:</span><span class="sxs-lookup"><span data-stu-id="8ad22-208">These are the values returned:</span></span></p>
<p><span data-ttu-id="8ad22-209">Wert</span><span class="sxs-lookup"><span data-stu-id="8ad22-209">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="8ad22-210">0</span><span class="sxs-lookup"><span data-stu-id="8ad22-210">0</span></span></li>
<li><span data-ttu-id="8ad22-211">1</span><span class="sxs-lookup"><span data-stu-id="8ad22-211">1</span></span></li>
<li><span data-ttu-id="8ad22-212">2</span><span class="sxs-lookup"><span data-stu-id="8ad22-212">2</span></span></li>
<li><span data-ttu-id="8ad22-213">3</span><span class="sxs-lookup"><span data-stu-id="8ad22-213">3</span></span></li>
<li><span data-ttu-id="8ad22-214">4</span><span class="sxs-lookup"><span data-stu-id="8ad22-214">4</span></span></li>
<li><span data-ttu-id="8ad22-215">5</span><span class="sxs-lookup"><span data-stu-id="8ad22-215">5</span></span></li>
<li><span data-ttu-id="8ad22-216">6</span><span class="sxs-lookup"><span data-stu-id="8ad22-216">6</span></span></li>
<li><span data-ttu-id="8ad22-217">7</span><span class="sxs-lookup"><span data-stu-id="8ad22-217">7</span></span></li>
<li><span data-ttu-id="8ad22-218">8</span><span class="sxs-lookup"><span data-stu-id="8ad22-218">8</span></span></li>
<li><span data-ttu-id="8ad22-219">9</span><span class="sxs-lookup"><span data-stu-id="8ad22-219">9</span></span></li>
<li><span data-ttu-id="8ad22-220">10</span><span class="sxs-lookup"><span data-stu-id="8ad22-220">10</span></span></li>
<li><span data-ttu-id="8ad22-221">11</span><span class="sxs-lookup"><span data-stu-id="8ad22-221">11</span></span></li>
<li><span data-ttu-id="8ad22-222">12</span><span class="sxs-lookup"><span data-stu-id="8ad22-222">12</span></span></li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-223">NextRow</span><span class="sxs-lookup"><span data-stu-id="8ad22-223">NextRow</span></span></p></td>
<td><p><span data-ttu-id="8ad22-224">Die Daten in der nächsten Zeile in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8ad22-224">The data in the next row in the table or query.</span></span> <span data-ttu-id="8ad22-225">Wenn Sie einen Kanal öffnen, gibt NextRow die Daten in der ersten Zeile zurück.</span><span class="sxs-lookup"><span data-stu-id="8ad22-225">When you open a channel, NextRow returns the data in the first row.</span></span> <span data-ttu-id="8ad22-226">Wenn die aktuelle Zeile der letzte Datensatz ist und Sie NextRow ausführen, schlägt die Anforderung fehl.</span><span class="sxs-lookup"><span data-stu-id="8ad22-226">If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-227">PrevRow</span><span class="sxs-lookup"><span data-stu-id="8ad22-227">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="8ad22-228">Die Daten in der vorherigen Zeile in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8ad22-228">The data in the previous row in the table or query.</span></span> <span data-ttu-id="8ad22-229">Wenn PrevRow die erste Anforderung eines neuen Kanals ist, werden die Daten in der letzten Zeile der Tabelle oder Abfrage zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ad22-229">If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned.</span></span> <span data-ttu-id="8ad22-230">Wenn der erste Datensatz die aktuelle Zeile ist, schlägt die Anforderung für PrevRow fehl.</span><span class="sxs-lookup"><span data-stu-id="8ad22-230">If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-231">FirstRow</span><span class="sxs-lookup"><span data-stu-id="8ad22-231">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="8ad22-232">Die Daten in der ersten Zeile der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8ad22-232">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-233">LastRow</span><span class="sxs-lookup"><span data-stu-id="8ad22-233">LastRow</span></span></p></td>
<td><p><span data-ttu-id="8ad22-234">Die Daten in der letzten Zeile der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8ad22-234">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-235">FieldCount</span><span class="sxs-lookup"><span data-stu-id="8ad22-235">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="8ad22-236">Die Anzahl der Felder in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8ad22-236">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad22-237">SQLText</span><span class="sxs-lookup"><span data-stu-id="8ad22-237">SQLText</span></span></p></td>
<td><p><span data-ttu-id="8ad22-238">Eine SQL-Anweisung, die die Tabelle oder Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="8ad22-238">An SQL statement representing the table or query.</span></span> <span data-ttu-id="8ad22-239">Bei Tabellen gibt dieses Element eine SQL-Anweisung im Formular &quot;Select `*` from <em>Table</em>zurück; &quot;.</span><span class="sxs-lookup"><span data-stu-id="8ad22-239">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad22-240">SQLTEXT <em>n</em></span><span class="sxs-lookup"><span data-stu-id="8ad22-240">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="8ad22-241">Eine SQL-Anweisung in <em>n</em>-Zeichen-Chunks, die die Tabelle oder Abfrage darstellt, wobei <em>n</em> eine ganze Zahl bis zu 256 ist.</span><span class="sxs-lookup"><span data-stu-id="8ad22-241">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="8ad22-242">Angenommen, eine Abfrage wird durch die folgende SQL-Anweisung dargestellt &quot;: das Element SQLTEXT; 7&quot; gibt die folgenden durch Tabulatoren getrennten Segmente zurück: das Element &quot;SQLTEXT; 7&quot; gibt die folgenden durch Tabstopps getrennten Abschnitte zurück:</span><span class="sxs-lookup"><span data-stu-id="8ad22-242">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="8ad22-243">Das folgende Beispiel zeigt, wie Sie mithilfe von DDE in einer Visual Basic-Prozedur Daten aus einer Tabelle in der Northwind-Beispieldatenbank anfordern und diese Daten in eine Textdatei einfügen können:</span><span class="sxs-lookup"><span data-stu-id="8ad22-243">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
