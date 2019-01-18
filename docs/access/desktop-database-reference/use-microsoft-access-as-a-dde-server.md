---
title: Verwenden von Microsoft Access als DDE-Server
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access unterstützt dynamischem Datenaustausch (DDE) als eine Anwendung Ziel (Client) oder quellanwendung (Server).
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716376"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="b7b30-103">Verwenden von Microsoft Access als DDE-Server</span><span class="sxs-lookup"><span data-stu-id="b7b30-103">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="b7b30-104">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7b30-104">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="b7b30-105">Microsoft Access unterstützt dynamischem Datenaustausch (DDE) als eine Anwendung Ziel (Client) oder quellanwendung (Server).</span><span class="sxs-lookup"><span data-stu-id="b7b30-105">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span> <span data-ttu-id="b7b30-106">Beispielsweise kann eine Anwendung wie Microsoft Word, der als ein Client fungiert Daten über DDE aus einer Microsoft Access-Datenbank anfordern, der als Server fungiert.</span><span class="sxs-lookup"><span data-stu-id="b7b30-106">For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="b7b30-107">Wenn Sie Microsoft Access-Objekte aus einer anderen Anwendung bearbeiten müssen, können Sie Automatisierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b7b30-107">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="b7b30-108">Eine DDE-Verbindung zwischen einem Client und Server wird zu einem bestimmten Thema eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="b7b30-108">A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="b7b30-109">Ein Thema kann entweder eine Datendatei im Format von der Serveranwendung unterstützt werden, oder es kann sein, das Thema "System", die Informationen über die Serveranwendung selbst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b7b30-109">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="b7b30-110">Nachdem Sie eine Unterhaltung zu einem bestimmten Thema begonnen hat, kann nur ein mit diesem Thema verbundenes Datenelement übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="b7b30-110">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="b7b30-111">Nehmen wir beispielsweise bei Microsoft Word ausgeführt werden und Daten aus einer bestimmten Microsoft Access-Datenbank in ein Dokument einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="b7b30-111">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document.</span></span> <span data-ttu-id="b7b30-112">Sie zunächst eine DDE-Verbindung mit Microsoft Access öffnen einen DDE-Kanal mit der **DDEInitiate** -Funktion und der Name der Datenbankdatei als Thema angeben.</span><span class="sxs-lookup"><span data-stu-id="b7b30-112">You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic.</span></span> <span data-ttu-id="b7b30-113">Sie können dann Daten aus dieser Datenbank an Microsoft Word über den Kanal übertragen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-113">You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="b7b30-114">Als DDE-Server unterstützt Microsoft Access die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b7b30-114">As a DDE server, Microsoft Access supports the following topics:</span></span>

- <span data-ttu-id="b7b30-115">Das Thema "System"</span><span class="sxs-lookup"><span data-stu-id="b7b30-115">The System topic</span></span>

- <span data-ttu-id="b7b30-116">Der Name einer Datenbank (Thema*Datenbank* )</span><span class="sxs-lookup"><span data-stu-id="b7b30-116">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="b7b30-117">Der Name einer Tabelle (Thema*Tabellenname* )</span><span class="sxs-lookup"><span data-stu-id="b7b30-117">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="b7b30-118">Der Name einer Abfrage (Thema*Abfragename* )</span><span class="sxs-lookup"><span data-stu-id="b7b30-118">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="b7b30-119">Eine Microsoft Access SQL-Zeichenfolge (Thema*SQLZeichenfolge* )</span><span class="sxs-lookup"><span data-stu-id="b7b30-119">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="b7b30-120">Nachdem Sie eine DDE-Verbindung hergestellt haben, können Sie die Anweisung **DDEExecute** , einen Befehl vom Client an die Server-Anwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="b7b30-120">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="b7b30-121">Wenn als DDE-Server verwendet wird, erkennt Microsoft Access die folgenden Befehle als gültig:</span><span class="sxs-lookup"><span data-stu-id="b7b30-121">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="b7b30-122">Der Name eines Makros in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b7b30-122">The name of a macro in the current database.</span></span>

- <span data-ttu-id="b7b30-123">Alle Aktionen, die Sie in Visual Basic können mithilfe der Methoden des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b7b30-123">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="b7b30-124">Die OpenDatabase und SchließenDatenbank-Aktionen, die nur für DDE-Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7b30-124">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations.</span></span> <span data-ttu-id="b7b30-125">(Ein Beispiel dafür, wie Sie diese Aktionen verwenden, finden Sie weiter unten in diesem Thema.)</span><span class="sxs-lookup"><span data-stu-id="b7b30-125">(For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="b7b30-126">Wenn Sie eine Makroaktion als Anweisung **DDEExecute** angeben, die Aktion und Argumenten führen Sie die Syntax der **DoCmd** -Objekt und müssen in Klammern ([]) eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b7b30-126">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]).</span></span> <span data-ttu-id="b7b30-127">Allerdings erkennen, die DDE unterstützen keine systeminterne Konstanten in DDE-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="b7b30-127">However, applications that support DDE don't recognize intrinsic constants in DDE operations.</span></span> <span data-ttu-id="b7b30-128">Darüber hinaus Zeichenfolgenargumente müssen in Anführungszeichen eingeschlossen werden (""), wenn die Zeichenfolge ein Komma enthält.</span><span class="sxs-lookup"><span data-stu-id="b7b30-128">Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma.</span></span> <span data-ttu-id="b7b30-129">Anderenfalls sind Anführungszeichen nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b7b30-129">Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="b7b30-130">Die Client-Anwendung können Sie die **DDERequest** -Funktion Textdaten aus der Serveranwendung über einen geöffneten DDE-Kanal verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7b30-130">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="b7b30-131">Oder der Client kann die Anweisung **DDEPoke** zum Senden von Daten an die Serveranwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7b30-131">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="b7b30-132">Nachdem die Datenübertragung abgeschlossen ist, kann der Client die Anweisung **DDETerminate** zum Schließen des DDE-Kanals oder der **DDETerminateAll** -Anweisung zum Schließen aller offenen Kanäle verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7b30-132">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="b7b30-133">Wenn die Clientanwendung empfangen von Daten über einen DDE-Kanal beendet wurde, sollte es den Kanal um Speicherressourcen zu sparen schließen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-133">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>

<span data-ttu-id="b7b30-134">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Microsoft Word-Prozedur mit Visual Basic erstellen, die Microsoft Access als DDE-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7b30-134">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server.</span></span> <span data-ttu-id="b7b30-135">(Für das Beispiel funktioniert, muss Microsoft Access ausgeführt werden.)</span><span class="sxs-lookup"><span data-stu-id="b7b30-135">(For this example to work, Microsoft Access must be running.)</span></span>

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

<span data-ttu-id="b7b30-136">Die folgenden Abschnitte enthalten Informationen zu den gültigen DDE-Themen, die von Microsoft Access unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7b30-136">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="b7b30-137">Das Thema "System"</span><span class="sxs-lookup"><span data-stu-id="b7b30-137">The System topic</span></span>

<span data-ttu-id="b7b30-138">Das Systemthema befindet sich standard für alle Microsoft Windows-basierten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-138">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="b7b30-139">Es liefert Informationen zu den anderen Themen, die von der Anwendung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7b30-139">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="b7b30-140">Zugriff auf diese Informationen muss Code rufen Sie zunächst die **DDEInitiate** -Funktion mit dem Argument *Thema* , und klicken Sie dann die **DDERequest** -Anweisung mit einer der folgenden Angaben für das Argument *Element* ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-140">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7b30-141">Element</span><span class="sxs-lookup"><span data-stu-id="b7b30-141">Item</span></span></p></th>
<th><p><span data-ttu-id="b7b30-142">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b7b30-142">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-143">"SysItems" verwenden</span><span class="sxs-lookup"><span data-stu-id="b7b30-143">SysItems</span></span></p></td>
<td><p><span data-ttu-id="b7b30-144">Eine Liste der Elemente, die von dem Thema "System" in Microsoft Access unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7b30-144">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-145">Formate</span><span class="sxs-lookup"><span data-stu-id="b7b30-145">Formats</span></span></p></td>
<td><p><span data-ttu-id="b7b30-146">Eine Liste der Formate können Microsoft Access in die Zwischenablage kopieren.</span><span class="sxs-lookup"><span data-stu-id="b7b30-146">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-147">Status</span><span class="sxs-lookup"><span data-stu-id="b7b30-147">Status</span></span></p></td>
<td><p><span data-ttu-id="b7b30-148">&quot;Ausgelastet&quot; oder &quot;bereit&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7b30-148">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-149">Topics</span><span class="sxs-lookup"><span data-stu-id="b7b30-149">Topics</span></span></p></td>
<td><p><span data-ttu-id="b7b30-150">Eine Liste aller geöffneten Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="b7b30-150">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="b7b30-151">Das folgende Beispiel veranschaulicht die Verwendung der Funktionen **DDEInitiate** und **DDERequest** mit dem Thema System:</span><span class="sxs-lookup"><span data-stu-id="b7b30-151">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

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

## <a name="the-database-topic"></a><span data-ttu-id="b7b30-152">Das Thema Datenbank</span><span class="sxs-lookup"><span data-stu-id="b7b30-152">The database topic</span></span>

<span data-ttu-id="b7b30-153">Das Thema *Datenbank* ist der Dateiname einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b7b30-153">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="b7b30-154">Sie können entweder nur den Namen der (Nordwind) oder den Pfad der Erweiterung eingeben (C:\\Access\\Beispiele\\Nordwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="b7b30-154">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="b7b30-155">Nach dem start einer DDE-Verbindung mit der Datenbank können Sie eine Liste der Objekte in der Datenbank anfordern.</span><span class="sxs-lookup"><span data-stu-id="b7b30-155">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

> [!NOTE]
> <span data-ttu-id="b7b30-156">Sie können keine DDE verwenden, um Microsoft Access-Arbeitsgruppen-Informationsdatei abzufragen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-156">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>

<span data-ttu-id="b7b30-157">Das Thema *Datenbank* unterstützt die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="b7b30-157">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7b30-158">Element</span><span class="sxs-lookup"><span data-stu-id="b7b30-158">Item</span></span></p></th>
<th><p><span data-ttu-id="b7b30-159">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b7b30-159">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-160">TableList</span><span class="sxs-lookup"><span data-stu-id="b7b30-160">TableList</span></span></p></td>
<td><p><span data-ttu-id="b7b30-161">Eine Liste der Tabellen</span><span class="sxs-lookup"><span data-stu-id="b7b30-161">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-162">QueryList</span><span class="sxs-lookup"><span data-stu-id="b7b30-162">QueryList</span></span></p></td>
<td><p><span data-ttu-id="b7b30-163">Eine Liste von Abfragen</span><span class="sxs-lookup"><span data-stu-id="b7b30-163">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-164">FormList</span><span class="sxs-lookup"><span data-stu-id="b7b30-164">FormList</span></span></p></td>
<td><p><span data-ttu-id="b7b30-165">Eine Liste von Formularen</span><span class="sxs-lookup"><span data-stu-id="b7b30-165">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-166">ReportList</span><span class="sxs-lookup"><span data-stu-id="b7b30-166">ReportList</span></span></p></td>
<td><p><span data-ttu-id="b7b30-167">Eine Liste der Berichte</span><span class="sxs-lookup"><span data-stu-id="b7b30-167">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-168">MacroList</span><span class="sxs-lookup"><span data-stu-id="b7b30-168">MacroList</span></span></p></td>
<td><p><span data-ttu-id="b7b30-169">Eine Liste mit Makros</span><span class="sxs-lookup"><span data-stu-id="b7b30-169">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-170">ModuleList</span><span class="sxs-lookup"><span data-stu-id="b7b30-170">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="b7b30-171">Eine Liste der Module</span><span class="sxs-lookup"><span data-stu-id="b7b30-171">A list of modules</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-172">ViewList</span><span class="sxs-lookup"><span data-stu-id="b7b30-172">ViewList</span></span></p></td>
<td><p><span data-ttu-id="b7b30-173">Eine Liste der Ansichten</span><span class="sxs-lookup"><span data-stu-id="b7b30-173">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-174">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="b7b30-174">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="b7b30-175">Eine Liste von gespeicherten Prozeduren</span><span class="sxs-lookup"><span data-stu-id="b7b30-175">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-176">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="b7b30-176">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="b7b30-177">Eine Liste der Datenbankdiagramme</span><span class="sxs-lookup"><span data-stu-id="b7b30-177">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="b7b30-178">Das folgende Beispiel zeigt, wie Sie das Formular Personal in der Northwind-Beispieldatenbank aus einer Visual Basic-Prozedur öffnen können:</span><span class="sxs-lookup"><span data-stu-id="b7b30-178">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

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

## <a name="the-table-topic"></a><span data-ttu-id="b7b30-179">Das Thema Tabelle</span><span class="sxs-lookup"><span data-stu-id="b7b30-179">The TABLE topic</span></span>

<span data-ttu-id="b7b30-180">In diesen Themen verwenden Sie die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="b7b30-180">These topics use the following syntax:</span></span>

<span data-ttu-id="b7b30-181">_Databasename_ ; **Tabelle** _TableName_</span><span class="sxs-lookup"><span data-stu-id="b7b30-181">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="b7b30-182">_Databasename_ ; **Abfrage** _Abfragename_</span><span class="sxs-lookup"><span data-stu-id="b7b30-182">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="b7b30-183">_Databasename_ ; **SQL** [ _Sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="b7b30-183">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7b30-184">Teil</span><span class="sxs-lookup"><span data-stu-id="b7b30-184">Part</span></span></p></th>
<th><p><span data-ttu-id="b7b30-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7b30-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-186"><em>Datenbankname</em></span><span class="sxs-lookup"><span data-stu-id="b7b30-186"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="b7b30-187">Der Name der Datenbank, die die Tabelle oder Abfrage in ist oder, die die SQL-Anweisung betrifft, gefolgt von einem Semikolon (;).</span><span class="sxs-lookup"><span data-stu-id="b7b30-187">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;).</span></span> <span data-ttu-id="b7b30-188">Der Name der Datenbank kann nur den Namen der (Nordwind) oder der vollständige Pfad und MDB-Erweiterung (C:\Access\Samples\Northwind.mdb) sein.</span><span class="sxs-lookup"><span data-stu-id="b7b30-188">The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-189"><em>TableName</em></span><span class="sxs-lookup"><span data-stu-id="b7b30-189"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="b7b30-190">Der Name einer vorhandenen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b7b30-190">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-191"><em>Abfragename</em></span><span class="sxs-lookup"><span data-stu-id="b7b30-191"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="b7b30-192">Der Name einer vorhandenen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b7b30-192">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-193"><em>SqlString</em></span><span class="sxs-lookup"><span data-stu-id="b7b30-193"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="b7b30-194">Eine gültige SQL­Anweisung bis zu 256 Zeichen lang sein, mit einem Semikolon enden.</span><span class="sxs-lookup"><span data-stu-id="b7b30-194">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="b7b30-195">Um mehr als 256 Zeichen austauschen möchten, geben Sie dieses Argument und stattdessen verwenden Sie aufeinander folgenden <strong>DDEPoke</strong> -Anweisungen zum Erstellen einer SQL-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b7b30-195">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="b7b30-196">Der folgenden Visual Basic-Code wird beispielsweise die Anweisung <strong>DDEPoke</strong> So erstellen eine SQL-Anweisung, und fordern Sie dann die Ergebnisse der Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7b30-196">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="b7b30-197">In der folgenden Tabelle sind die gültigen Elemente für die Tabelle *Tabellenname*, QUERY *Abfragename*und SQL *SQLZeichenfolge* Themen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-197">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7b30-198">Element</span><span class="sxs-lookup"><span data-stu-id="b7b30-198">Item</span></span></p></th>
<th><p><span data-ttu-id="b7b30-199">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b7b30-199">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-200">Alle</span><span class="sxs-lookup"><span data-stu-id="b7b30-200">All</span></span></p></td>
<td><p><span data-ttu-id="b7b30-201">Die Daten in der Tabelle, einschließlich Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-201">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-202">Daten</span><span class="sxs-lookup"><span data-stu-id="b7b30-202">Data</span></span></p></td>
<td><p><span data-ttu-id="b7b30-203">Alle Zeilen mit Daten, ohne Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-203">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-204">FieldNames</span><span class="sxs-lookup"><span data-stu-id="b7b30-204">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="b7b30-205">Eine einzeilige Liste von Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-205">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-206">FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="b7b30-206">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="b7b30-207">Eine zwei Zeilen Liste von Feldnamen (erste Zeile) und deren Datentypen (zweite Zeile).</span><span class="sxs-lookup"><span data-stu-id="b7b30-207">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="b7b30-208">Dies sind die zurückgegebenen Werte:</span><span class="sxs-lookup"><span data-stu-id="b7b30-208">These are the values returned:</span></span></p>
<p><span data-ttu-id="b7b30-209">Wert</span><span class="sxs-lookup"><span data-stu-id="b7b30-209">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="b7b30-210">0</span><span class="sxs-lookup"><span data-stu-id="b7b30-210">0</span></span></li>
<li><span data-ttu-id="b7b30-211">1</span><span class="sxs-lookup"><span data-stu-id="b7b30-211">1</span></span></li>
<li><span data-ttu-id="b7b30-212">2</span><span class="sxs-lookup"><span data-stu-id="b7b30-212">2</span></span></li>
<li><span data-ttu-id="b7b30-213">3</span><span class="sxs-lookup"><span data-stu-id="b7b30-213">3</span></span></li>
<li><span data-ttu-id="b7b30-214">4</span><span class="sxs-lookup"><span data-stu-id="b7b30-214">4</span></span></li>
<li><span data-ttu-id="b7b30-215">5</span><span class="sxs-lookup"><span data-stu-id="b7b30-215">5</span></span></li>
<li><span data-ttu-id="b7b30-216">6</span><span class="sxs-lookup"><span data-stu-id="b7b30-216">6</span></span></li>
<li><span data-ttu-id="b7b30-217">7</span><span class="sxs-lookup"><span data-stu-id="b7b30-217">7</span></span></li>
<li><span data-ttu-id="b7b30-218">8</span><span class="sxs-lookup"><span data-stu-id="b7b30-218">8</span></span></li>
<li><span data-ttu-id="b7b30-219">9</span><span class="sxs-lookup"><span data-stu-id="b7b30-219">9</span></span></li>
<li><span data-ttu-id="b7b30-220">10</span><span class="sxs-lookup"><span data-stu-id="b7b30-220">10</span></span></li>
<li><span data-ttu-id="b7b30-221">11</span><span class="sxs-lookup"><span data-stu-id="b7b30-221">11</span></span></li>
<li><span data-ttu-id="b7b30-222">12</span><span class="sxs-lookup"><span data-stu-id="b7b30-222">12</span></span></li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-223">NextRow</span><span class="sxs-lookup"><span data-stu-id="b7b30-223">NextRow</span></span></p></td>
<td><p><span data-ttu-id="b7b30-224">Die Daten in der nächsten Zeile in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b7b30-224">The data in the next row in the table or query.</span></span> <span data-ttu-id="b7b30-225">Wenn Sie einen Kanal öffnen, gibt NextRow die Daten in der ersten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b7b30-225">When you open a channel, NextRow returns the data in the first row.</span></span> <span data-ttu-id="b7b30-226">Wenn die aktuelle Zeile der letzte Datensatz ist und Ausführung von NextRow, schlägt die Anforderung fehl.</span><span class="sxs-lookup"><span data-stu-id="b7b30-226">If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-227">Fehl</span><span class="sxs-lookup"><span data-stu-id="b7b30-227">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="b7b30-228">Die Daten in der vorherigen Zeile in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b7b30-228">The data in the previous row in the table or query.</span></span> <span data-ttu-id="b7b30-229">Wenn fehl die erste Anforderung über einen neuen Kanal ist, werden die Daten in der letzten Zeile der Tabelle oder Abfrage zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7b30-229">If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned.</span></span> <span data-ttu-id="b7b30-230">Wenn der erste Datensatz der aktuelle Zeile ist, schlägt die Anforderung fehl.</span><span class="sxs-lookup"><span data-stu-id="b7b30-230">If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-231">FirstRow</span><span class="sxs-lookup"><span data-stu-id="b7b30-231">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="b7b30-232">Die Daten in der ersten Zeile der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b7b30-232">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-233">LastRow</span><span class="sxs-lookup"><span data-stu-id="b7b30-233">LastRow</span></span></p></td>
<td><p><span data-ttu-id="b7b30-234">Die Daten in der letzten Zeile der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b7b30-234">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-235">FieldCount</span><span class="sxs-lookup"><span data-stu-id="b7b30-235">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="b7b30-236">Die Anzahl der Felder in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b7b30-236">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7b30-237">SQLText</span><span class="sxs-lookup"><span data-stu-id="b7b30-237">SQLText</span></span></p></td>
<td><p><span data-ttu-id="b7b30-238">Eine SQL-Anweisung, die die Tabelle oder Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="b7b30-238">An SQL statement representing the table or query.</span></span> <span data-ttu-id="b7b30-239">Für Tabellen, gibt dieses Element eine SQL-Anweisung in der Form &quot;auswählen `*` FROM <em>Tabelle</em>; &quot;.</span><span class="sxs-lookup"><span data-stu-id="b7b30-239">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7b30-240">SQLText; <em>n</em></span><span class="sxs-lookup"><span data-stu-id="b7b30-240">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="b7b30-241">Eine SQL­Anweisung in <em>n</em>-Segmenten für eine Tabelle oder Abfrage, wobei <em>n</em> eine ganze Zahl bis zu 256 ist Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b7b30-241">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="b7b30-242">Nehmen wir beispielsweise bei eine Abfrage wird durch die folgende SQL-Anweisung dargestellt: das Element &quot;SQLText; 7&quot; gibt die folgenden Abschnitte Tabstopp-getrennt: das Element &quot;SQLText; 7&quot; gibt die folgenden Abschnitte Tabstopp-getrennt:</span><span class="sxs-lookup"><span data-stu-id="b7b30-242">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="b7b30-243">Das folgende Beispiel zeigt, wie Sie DDE in einer Visual Basic-Prozedur das Abrufen von Daten aus einer Tabelle in der Northwind-Beispieldatenbank verwenden und diese Daten in eine Textdatei einfügen:</span><span class="sxs-lookup"><span data-stu-id="b7b30-243">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

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
