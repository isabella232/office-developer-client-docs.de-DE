---
title: Verwenden von Microsoft Access als DDE-server
TOCTitle: Use Microsoft Access as a DDE Server
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 84b4e30877488d84e03839764c1996053e76a2e7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475184"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="6c1c3-102">Verwenden von Microsoft Access als DDE-server</span><span class="sxs-lookup"><span data-stu-id="6c1c3-102">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="6c1c3-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c1c3-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="6c1c3-104">Microsoft Access unterstützt dynamischem Datenaustausch (DDE) als eine Anwendung Ziel (Client) oder quellanwendung (Server).</span><span class="sxs-lookup"><span data-stu-id="6c1c3-104">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span> <span data-ttu-id="6c1c3-105">Beispielsweise kann eine Anwendung wie Microsoft Word, der als ein Client fungiert Daten über DDE aus einer Microsoft Access-Datenbank anfordern, der als Server fungiert.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-105">For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="6c1c3-106">Wenn Sie Microsoft Access-Objekte aus einer anderen Anwendung bearbeiten müssen, können Sie Automatisierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-106">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="6c1c3-107">Eine DDE-Verbindung zwischen einem Client und Server wird zu einem bestimmten Thema eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-107">A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="6c1c3-108">Ein Thema kann entweder eine Datendatei im Format von der Serveranwendung unterstützt werden, oder es kann sein, das Thema "System", die Informationen über die Serveranwendung selbst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-108">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="6c1c3-109">Nachdem eine Unterhaltung zu einem bestimmten Thema begonnen hat, kann nur ein mit diesem Thema verbundenes Datenelement übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-109">Once a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="6c1c3-110">Nehmen wir beispielsweise bei Microsoft Word ausgeführt werden und Daten aus einer bestimmten Microsoft Access-Datenbank in ein Dokument einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-110">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document.</span></span> <span data-ttu-id="6c1c3-111">Sie zunächst eine DDE-Verbindung mit Microsoft Access öffnen einen DDE-Kanal mit der **DDEInitiate** -Funktion und der Name der Datenbankdatei als Thema angeben.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-111">You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic.</span></span> <span data-ttu-id="6c1c3-112">Sie können dann Daten aus dieser Datenbank an Microsoft Word über den Kanal übertragen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-112">You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="6c1c3-113">Als DDE-Server unterstützt Microsoft Access die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6c1c3-113">As a DDE server, Microsoft Access supports the following topics:</span></span>

  - <span data-ttu-id="6c1c3-114">Das Thema "System"</span><span class="sxs-lookup"><span data-stu-id="6c1c3-114">The System topic</span></span>

  - <span data-ttu-id="6c1c3-115">Der Name einer Datenbank (Thema*Datenbank* )</span><span class="sxs-lookup"><span data-stu-id="6c1c3-115">The name of a database (*database* topic)</span></span>

  - <span data-ttu-id="6c1c3-116">Der Name einer Tabelle (Thema*Tabellenname* )</span><span class="sxs-lookup"><span data-stu-id="6c1c3-116">The name of a table (*tablename* topic)</span></span>

  - <span data-ttu-id="6c1c3-117">Der Name einer Abfrage (Thema*Abfragename* )</span><span class="sxs-lookup"><span data-stu-id="6c1c3-117">The name of a query (*queryname* topic)</span></span>

  - <span data-ttu-id="6c1c3-118">Eine Microsoft Access SQL-Zeichenfolge (Thema*SQLZeichenfolge* )</span><span class="sxs-lookup"><span data-stu-id="6c1c3-118">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="6c1c3-119">Nachdem Sie eine DDE-Verbindung hergestellt haben, können Sie die Anweisung **DDEExecute** , einen Befehl vom Client an die Server-Anwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-119">Once you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="6c1c3-120">Wenn als DDE-Server verwendet wird, erkennt Microsoft Access die folgenden Befehle als gültig:</span><span class="sxs-lookup"><span data-stu-id="6c1c3-120">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

  - <span data-ttu-id="6c1c3-121">Der Name eines Makros in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-121">The name of a macro in the current database.</span></span>

  - <span data-ttu-id="6c1c3-122">Alle Aktionen, die Sie in Visual Basic können mithilfe der Methoden des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-122">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

  - <span data-ttu-id="6c1c3-123">Die OpenDatabase und SchließenDatenbank-Aktionen, die nur für DDE-Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-123">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations.</span></span> <span data-ttu-id="6c1c3-124">(Ein Beispiel dafür, wie Sie diese Aktionen verwenden, finden Sie weiter unten in diesem Thema.)</span><span class="sxs-lookup"><span data-stu-id="6c1c3-124">(For an example of how to use these actions, see the example later in this topic.)</span></span>


> [!NOTE]
> <P><span data-ttu-id="6c1c3-125">Wenn Sie eine Makroaktion als Anweisung <STRONG>DDEExecute</STRONG> angeben, die Aktion und Argumenten führen Sie die Syntax der <STRONG>DoCmd</STRONG> -Objekt und müssen in Klammern ([]) eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-125">When you specify a macro action as a <STRONG>DDEExecute</STRONG> statement, the action and any arguments follow the <STRONG>DoCmd</STRONG> object syntax and must be enclosed in brackets ([ ]).</span></span> <span data-ttu-id="6c1c3-126">Allerdings erkennen, die DDE unterstützen keine systeminterne Konstanten in DDE-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-126">However, applications that support DDE don't recognize intrinsic constants in DDE operations.</span></span> <span data-ttu-id="6c1c3-127">Darüber hinaus Zeichenfolgenargumente müssen in Anführungszeichen eingeschlossen werden (""), wenn die Zeichenfolge ein Komma enthält.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-127">Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma.</span></span> <span data-ttu-id="6c1c3-128">Anderenfalls sind Anführungszeichen nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-128">Otherwise, quotation marks aren't required.</span></span></P>



<span data-ttu-id="6c1c3-129">Die Client-Anwendung können Sie die **DDERequest** -Funktion Textdaten aus der Serveranwendung über einen geöffneten DDE-Kanal verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-129">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="6c1c3-130">Oder der Client kann die Anweisung **DDEPoke** zum Senden von Daten an die Serveranwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-130">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="6c1c3-131">Sobald die Datenübertragung abgeschlossen ist, kann der Client die Anweisung **DDETerminate** zum Schließen des DDE-Kanals oder der **DDETerminateAll** -Anweisung zum Schließen aller geöffneten Kanäle verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-131">Once the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6c1c3-132">Wenn die Clientanwendung empfangen von Daten über einen DDE-Kanal beendet wurde, sollte es den Kanal um Speicherressourcen zu sparen schließen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-132">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span></P>



<span data-ttu-id="6c1c3-133">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Microsoft Word-Prozedur mit Visual Basic erstellen, die Microsoft Access als DDE-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-133">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server.</span></span> <span data-ttu-id="6c1c3-134">(Für das Beispiel funktioniert, muss Microsoft Access ausgeführt werden.)</span><span class="sxs-lookup"><span data-stu-id="6c1c3-134">(For this example to work, Microsoft Access must be running.)</span></span>

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

<span data-ttu-id="6c1c3-135">Die folgenden Abschnitte enthalten Informationen zu den gültigen DDE-Themen, die von Microsoft Access unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-135">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="6c1c3-136">Das Thema "System"</span><span class="sxs-lookup"><span data-stu-id="6c1c3-136">The System topic</span></span>

<span data-ttu-id="6c1c3-137">Das Systemthema befindet sich standard für alle Microsoft Windows-basierten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-137">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="6c1c3-138">Es liefert Informationen zu den anderen Themen, die von der Anwendung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-138">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="6c1c3-139">Zugriff auf diese Informationen muss Code rufen Sie zunächst die **DDEInitiate** -Funktion mit als Argument *Thema* , und klicken Sie dann die **DDERequest** -Anweisung mit einer der folgenden Angaben für das Argument *Element* ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-139">To access this information, your code must first call the **DDEInitiate** function with as the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c1c3-140">Element</span><span class="sxs-lookup"><span data-stu-id="6c1c3-140">Item</span></span></p></th>
<th><p><span data-ttu-id="6c1c3-141">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6c1c3-141">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-142">"SysItems" verwenden</span><span class="sxs-lookup"><span data-stu-id="6c1c3-142">SysItems</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-143">Eine Liste der Elemente, die von dem Thema "System" in Microsoft Access unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-143">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-144">Formate</span><span class="sxs-lookup"><span data-stu-id="6c1c3-144">Formats</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-145">Eine Liste der Formate können Microsoft Access in die Zwischenablage kopieren.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-145">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-146">Status</span><span class="sxs-lookup"><span data-stu-id="6c1c3-146">Status</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-147">&quot;Ausgelastet&quot; oder &quot;bereit&quot;.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-147">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-148">Topics</span><span class="sxs-lookup"><span data-stu-id="6c1c3-148">Topics</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-149">Eine Liste aller geöffneten Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-149">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c1c3-150">Das folgende Beispiel veranschaulicht die Verwendung der Funktionen **DDEInitiate** und **DDERequest** mit dem Thema System:</span><span class="sxs-lookup"><span data-stu-id="6c1c3-150">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

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

## <a name="the-database-topic"></a><span data-ttu-id="6c1c3-151">Das Thema Datenbank</span><span class="sxs-lookup"><span data-stu-id="6c1c3-151">The database topic</span></span>

<span data-ttu-id="6c1c3-152">Das Thema *Datenbank* ist der Dateiname einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-152">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="6c1c3-153">Sie können entweder nur den Namen der (Nordwind) oder den Pfad der Erweiterung eingeben (C:\\Access\\Beispiele\\Nordwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="6c1c3-153">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="6c1c3-154">Nach dem start einer DDE-Verbindung mit der Datenbank können Sie eine Liste der Objekte in der Datenbank anfordern.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-154">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6c1c3-155">Sie können keine DDE verwenden, um Microsoft Access-Arbeitsgruppen-Informationsdatei abzufragen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-155">You can't use DDE to query the Microsoft Access workgroup information file.</span></span></P>



<span data-ttu-id="6c1c3-156">Das Thema *Datenbank* unterstützt die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-156">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c1c3-157">Element</span><span class="sxs-lookup"><span data-stu-id="6c1c3-157">Item</span></span></p></th>
<th><p><span data-ttu-id="6c1c3-158">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6c1c3-158">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-159">TableList</span><span class="sxs-lookup"><span data-stu-id="6c1c3-159">TableList</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-160">Eine Liste der Tabellen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-160">A list of tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-161">QueryList</span><span class="sxs-lookup"><span data-stu-id="6c1c3-161">QueryList</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-162">Eine Liste von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-162">A list of queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-163">FormList</span><span class="sxs-lookup"><span data-stu-id="6c1c3-163">FormList</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-164">Eine Liste von Formularen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-164">A list of forms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-165">ReportList</span><span class="sxs-lookup"><span data-stu-id="6c1c3-165">ReportList</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-166">Eine Liste der Berichte.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-166">A list of reports.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-167">MacroList</span><span class="sxs-lookup"><span data-stu-id="6c1c3-167">MacroList</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-168">Eine Liste mit Makros.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-168">A list of macros.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-169">ModuleList</span><span class="sxs-lookup"><span data-stu-id="6c1c3-169">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-170">Eine Liste von Modulen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-170">A list of modules.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-171">ViewList</span><span class="sxs-lookup"><span data-stu-id="6c1c3-171">ViewList</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-172">Eine Liste der Ansichten</span><span class="sxs-lookup"><span data-stu-id="6c1c3-172">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-173">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="6c1c3-173">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-174">Eine Liste von gespeicherten Prozeduren</span><span class="sxs-lookup"><span data-stu-id="6c1c3-174">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-175">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="6c1c3-175">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-176">Eine Liste der Datenbankdiagramme</span><span class="sxs-lookup"><span data-stu-id="6c1c3-176">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c1c3-177">Das folgende Beispiel zeigt, wie Sie das Formular Personal in der Northwind-Beispieldatenbank aus einer Visual Basic-Prozedur öffnen können:</span><span class="sxs-lookup"><span data-stu-id="6c1c3-177">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

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

## <a name="the-table-topic"></a><span data-ttu-id="6c1c3-178">Das Thema Tabelle</span><span class="sxs-lookup"><span data-stu-id="6c1c3-178">The TABLE topic</span></span>

<span data-ttu-id="6c1c3-179">In diesen Themen verwenden Sie die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="6c1c3-179">These topics use the following syntax:</span></span>

<span data-ttu-id="6c1c3-180">_Databasename_ ; **Tabelle** _TableName_</span><span class="sxs-lookup"><span data-stu-id="6c1c3-180">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="6c1c3-181">_Databasename_ ; **Abfrage** _Abfragename_</span><span class="sxs-lookup"><span data-stu-id="6c1c3-181">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="6c1c3-182">_Databasename_ ; **SQL** [ _Sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="6c1c3-182">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c1c3-183">Teil</span><span class="sxs-lookup"><span data-stu-id="6c1c3-183">Part</span></span></p></th>
<th><p><span data-ttu-id="6c1c3-184">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c1c3-184">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-185"><em>Datenbankname</em></span><span class="sxs-lookup"><span data-stu-id="6c1c3-185"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="6c1c3-186">Der Name der Datenbank, die die Tabelle oder Abfrage in ist oder, die die SQL-Anweisung betrifft, gefolgt von einem Semikolon (;).</span><span class="sxs-lookup"><span data-stu-id="6c1c3-186">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;).</span></span> <span data-ttu-id="6c1c3-187">Der Name der Datenbank kann nur den Namen der (Nordwind) oder der vollständige Pfad und MDB-Erweiterung (C:\Access\Samples\Northwind.mdb) sein.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-187">The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-188"><em>TableName</em></span><span class="sxs-lookup"><span data-stu-id="6c1c3-188"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="6c1c3-189">Der Name einer vorhandenen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-189">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-190"><em>Abfragename</em></span><span class="sxs-lookup"><span data-stu-id="6c1c3-190"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="6c1c3-191">Der Name einer vorhandenen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-191">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-192"><em>SqlString</em></span><span class="sxs-lookup"><span data-stu-id="6c1c3-192"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="6c1c3-193">Eine gültige SQL­Anweisung bis zu 256 Zeichen lang sein, mit einem Semikolon enden.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-193">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="6c1c3-194">Um mehr als 256 Zeichen austauschen möchten, geben Sie dieses Argument und stattdessen verwenden Sie aufeinander folgenden <strong>DDEPoke</strong> -Anweisungen zum Erstellen einer SQL-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-194">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="6c1c3-195">Der folgenden Visual Basic-Code wird beispielsweise die Anweisung <strong>DDEPoke</strong> So erstellen eine SQL-Anweisung, und fordern Sie dann die Ergebnisse der Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-195">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="6c1c3-196">In der folgenden Tabelle sind die gültigen Elemente für die Tabelle *Tabellenname*, QUERY *Abfragename*und SQL *SQLZeichenfolge* Themen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-196">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c1c3-197">Element</span><span class="sxs-lookup"><span data-stu-id="6c1c3-197">Item</span></span></p></th>
<th><p><span data-ttu-id="6c1c3-198">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6c1c3-198">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-199">Alle</span><span class="sxs-lookup"><span data-stu-id="6c1c3-199">All</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-200">Die Daten in der Tabelle, einschließlich Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-200">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-201">Daten</span><span class="sxs-lookup"><span data-stu-id="6c1c3-201">Data</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-202">Alle Zeilen mit Daten, ohne Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-202">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-203">FieldNames</span><span class="sxs-lookup"><span data-stu-id="6c1c3-203">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-204">Eine einzeilige Liste von Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-204">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-205">FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="6c1c3-205">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-206">Eine zwei Zeilen Liste von Feldnamen (erste Zeile) und deren Datentypen (zweite Zeile).</span><span class="sxs-lookup"><span data-stu-id="6c1c3-206">A two-row list of field names (first row) and their data types (second row).</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-207">Dies sind die zurückgegebenen Werte und die Datentypen, die sie darstellen:</span><span class="sxs-lookup"><span data-stu-id="6c1c3-207">These are the values returned and the data types they represent:</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-208"><b>Wert</b></span><span class="sxs-lookup"><span data-stu-id="6c1c3-208"><b>Value</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-209">0</span><span class="sxs-lookup"><span data-stu-id="6c1c3-209">0</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-210">1</span><span class="sxs-lookup"><span data-stu-id="6c1c3-210">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-211">2</span><span class="sxs-lookup"><span data-stu-id="6c1c3-211">2</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-212">3</span><span class="sxs-lookup"><span data-stu-id="6c1c3-212">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-213">4</span><span class="sxs-lookup"><span data-stu-id="6c1c3-213">4</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-214">5</span><span class="sxs-lookup"><span data-stu-id="6c1c3-214">5</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-215">6</span><span class="sxs-lookup"><span data-stu-id="6c1c3-215">6</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-216">7</span><span class="sxs-lookup"><span data-stu-id="6c1c3-216">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-217">8</span><span class="sxs-lookup"><span data-stu-id="6c1c3-217">8</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-218">9</span><span class="sxs-lookup"><span data-stu-id="6c1c3-218">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-219">10</span><span class="sxs-lookup"><span data-stu-id="6c1c3-219">10</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-220">11</span><span class="sxs-lookup"><span data-stu-id="6c1c3-220">11</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6c1c3-221">12</span><span class="sxs-lookup"><span data-stu-id="6c1c3-221">12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-222">NextRow</span><span class="sxs-lookup"><span data-stu-id="6c1c3-222">NextRow</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-223">Die Daten in der nächsten Zeile in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-223">The data in the next row in the table or query.</span></span> <span data-ttu-id="6c1c3-224">Wenn Sie einen Kanal öffnen, gibt NextRow die Daten in der ersten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-224">When you open a channel, NextRow returns the data in the first row.</span></span> <span data-ttu-id="6c1c3-225">Wenn die aktuelle Zeile der letzte Datensatz ist und Ausführung von NextRow, schlägt die Anforderung fehl.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-225">If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-226">Fehl</span><span class="sxs-lookup"><span data-stu-id="6c1c3-226">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-227">Die Daten in der vorherigen Zeile in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-227">The data in the previous row in the table or query.</span></span> <span data-ttu-id="6c1c3-228">Wenn fehl die erste Anforderung über einen neuen Kanal ist, werden die Daten in der letzten Zeile der Tabelle oder Abfrage zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-228">If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned.</span></span> <span data-ttu-id="6c1c3-229">Wenn der erste Datensatz der aktuelle Zeile ist, schlägt die Anforderung fehl.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-229">If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-230">FirstRow</span><span class="sxs-lookup"><span data-stu-id="6c1c3-230">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-231">Die Daten in der ersten Zeile der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-231">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-232">LastRow</span><span class="sxs-lookup"><span data-stu-id="6c1c3-232">LastRow</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-233">Die Daten in der letzten Zeile der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-233">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-234">FieldCount</span><span class="sxs-lookup"><span data-stu-id="6c1c3-234">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-235">Die Anzahl der Felder in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-235">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1c3-236">SQLText</span><span class="sxs-lookup"><span data-stu-id="6c1c3-236">SQLText</span></span></p></td>
<td><p><span data-ttu-id="6c1c3-237">Eine SQL-Anweisung, die die Tabelle oder Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-237">An SQL statement representing the table or query.</span></span> <span data-ttu-id="6c1c3-238">Für Tabellen, gibt dieses Element eine SQL-Anweisung in der Form &quot;auswählen `*` FROM <em>Tabelle</em>; &quot;.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-238">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1c3-239">SQLText; <em>n</em></span><span class="sxs-lookup"><span data-stu-id="6c1c3-239">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="6c1c3-240">Eine SQL­Anweisung in <em>n</em>-Segmenten für eine Tabelle oder Abfrage, wobei <em>n</em> eine ganze Zahl bis zu 256 ist Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6c1c3-240">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="6c1c3-241">Nehmen wir beispielsweise bei eine Abfrage wird durch die folgende SQL-Anweisung dargestellt: das Element &quot;SQLText; 7&quot; gibt die folgenden Abschnitte Tabstopp-getrennt: das Element &quot;SQLText; 7&quot; gibt die folgenden Abschnitte Tabstopp-getrennt:</span><span class="sxs-lookup"><span data-stu-id="6c1c3-241">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c1c3-242">Das folgende Beispiel zeigt, wie Sie DDE in einer Visual Basic-Prozedur das Abrufen von Daten aus einer Tabelle in der Northwind-Beispieldatenbank verwenden und diese Daten in eine Textdatei einfügen:</span><span class="sxs-lookup"><span data-stu-id="6c1c3-242">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

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
