---
<span data-ttu-id="e0d11-101">Titel: Verwenden von Microsoft Access als DDE-Server TOCTitle: Verwenden von Microsoft Access als DDE-Server <<<<<<< HEAD Ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 Ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) Ms:contentKeyID: 48546801 ms.date: 09/18/2015 === Beschreibung: Microsoft Access unterstützt dynamischem Datenaustausch (DDE) als eine Anwendung Ziel (Client) oder quellanwendung (Server).</span><span class="sxs-lookup"><span data-stu-id="e0d11-101">title: Use Microsoft Access as a DDE server TOCTitle: Use Microsoft Access as a DDE Server <<<<<<< HEAD ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 09/18/2015 ======= description: Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span>  
<span data-ttu-id="e0d11-102">MS:AssetId: a3e82bf7-94b5-8eec-86bc-2d5387d66738 Ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) Ms:contentKeyID: 48546801 ms.date: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="e0d11-102">ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="e0d11-103">Master-Shape Mtps_version: Office. 15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="e0d11-103">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="e0d11-104">vbaac10.chm5186349 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="e0d11-104">vbaac10.chm5186349 f1_categories:</span></span>
- <span data-ttu-id="e0d11-105">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="e0d11-105">Office.Version=v15</span></span>
---

# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="e0d11-106">Verwenden von Microsoft Access als DDE-server</span><span class="sxs-lookup"><span data-stu-id="e0d11-106">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="e0d11-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0d11-107">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="e0d11-108">Microsoft Access unterstützt dynamischem Datenaustausch (DDE) als eine Anwendung Ziel (Client) oder quellanwendung (Server).</span><span class="sxs-lookup"><span data-stu-id="e0d11-108">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span> <span data-ttu-id="e0d11-109">Beispielsweise kann eine Anwendung wie Microsoft Word, der als ein Client fungiert Daten über DDE aus einer Microsoft Access-Datenbank anfordern, der als Server fungiert.</span><span class="sxs-lookup"><span data-stu-id="e0d11-109">For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="e0d11-110">Wenn Sie Microsoft Access-Objekte aus einer anderen Anwendung bearbeiten müssen, können Sie Automatisierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="e0d11-110">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="e0d11-111"><<<<<<< HEAD eine DDE-Verbindung zwischen einem Client und Server wird zu einem bestimmten Thema eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e0d11-111"><<<<<<< HEAD A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="e0d11-112">Ein Thema kann entweder eine Datendatei im Format von der Serveranwendung unterstützt werden, oder es kann sein, das Thema "System", die Informationen über die Serveranwendung selbst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e0d11-112">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="e0d11-113">Nachdem eine Unterhaltung zu einem bestimmten Thema begonnen hat, kann nur ein mit diesem Thema verbundenes Datenelement übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-113">Once a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>
<span data-ttu-id="e0d11-114">=== Einer DDE-Verbindung zwischen einem Client und Server wird zu einem bestimmten Thema eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e0d11-114">======= A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="e0d11-115">Ein Thema kann entweder eine Datendatei im Format von der Serveranwendung unterstützt werden, oder es kann sein, das Thema "System", die Informationen über die Serveranwendung selbst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e0d11-115">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="e0d11-116">Nachdem Sie eine Unterhaltung zu einem bestimmten Thema begonnen hat, kann nur ein mit diesem Thema verbundenes Datenelement übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-116">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>
>>>>>>> <span data-ttu-id="e0d11-117">master</span><span class="sxs-lookup"><span data-stu-id="e0d11-117">master</span></span>

<span data-ttu-id="e0d11-118">Nehmen wir beispielsweise bei Microsoft Word ausgeführt werden und Daten aus einer bestimmten Microsoft Access-Datenbank in ein Dokument einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="e0d11-118">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document.</span></span> <span data-ttu-id="e0d11-119">Sie zunächst eine DDE-Verbindung mit Microsoft Access öffnen einen DDE-Kanal mit der **DDEInitiate** -Funktion und der Name der Datenbankdatei als Thema angeben.</span><span class="sxs-lookup"><span data-stu-id="e0d11-119">You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic.</span></span> <span data-ttu-id="e0d11-120">Sie können dann Daten aus dieser Datenbank an Microsoft Word über den Kanal übertragen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-120">You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="e0d11-121">Als DDE-Server unterstützt Microsoft Access die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e0d11-121">As a DDE server, Microsoft Access supports the following topics:</span></span>

<span data-ttu-id="e0d11-122"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e0d11-122"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="e0d11-123">Das Thema "System"</span><span class="sxs-lookup"><span data-stu-id="e0d11-123">The System topic</span></span>

  - <span data-ttu-id="e0d11-124">Der Name einer Datenbank (Thema*Datenbank* )</span><span class="sxs-lookup"><span data-stu-id="e0d11-124">The name of a database (*database* topic)</span></span>

  - <span data-ttu-id="e0d11-125">Der Name einer Tabelle (Thema*Tabellenname* )</span><span class="sxs-lookup"><span data-stu-id="e0d11-125">The name of a table (*tablename* topic)</span></span>

  - <span data-ttu-id="e0d11-126">Der Name einer Abfrage (Thema*Abfragename* )</span><span class="sxs-lookup"><span data-stu-id="e0d11-126">The name of a query (*queryname* topic)</span></span>

  - <span data-ttu-id="e0d11-127">Eine Microsoft Access SQL-Zeichenfolge (Thema*SQLZeichenfolge* )</span><span class="sxs-lookup"><span data-stu-id="e0d11-127">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="e0d11-128">Nachdem Sie eine DDE-Verbindung hergestellt haben, können Sie die Anweisung **DDEExecute** , einen Befehl vom Client an die Server-Anwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-128">Once you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="e0d11-129">Wenn als DDE-Server verwendet wird, erkennt Microsoft Access die folgenden Befehle als gültig:</span><span class="sxs-lookup"><span data-stu-id="e0d11-129">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

  - <span data-ttu-id="e0d11-130">Der Name eines Makros in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e0d11-130">The name of a macro in the current database.</span></span>

  - <span data-ttu-id="e0d11-131">Alle Aktionen, die Sie in Visual Basic können mithilfe der Methoden des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e0d11-131">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

  - <span data-ttu-id="e0d11-132">Die OpenDatabase und SchließenDatenbank-Aktionen, die nur für DDE-Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-132">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations.</span></span> <span data-ttu-id="e0d11-133">(Ein Beispiel dafür, wie Sie diese Aktionen verwenden, finden Sie weiter unten in diesem Thema.)</span><span class="sxs-lookup"><span data-stu-id="e0d11-133">(For an example of how to use these actions, see the example later in this topic.)</span></span>


> [!NOTE]
> <P><span data-ttu-id="e0d11-134">Wenn Sie eine Makroaktion als Anweisung <STRONG>DDEExecute</STRONG> angeben, die Aktion und Argumenten führen Sie die Syntax der <STRONG>DoCmd</STRONG> -Objekt und müssen in Klammern ([]) eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-134">When you specify a macro action as a <STRONG>DDEExecute</STRONG> statement, the action and any arguments follow the <STRONG>DoCmd</STRONG> object syntax and must be enclosed in brackets ([ ]).</span></span> <span data-ttu-id="e0d11-135">Allerdings erkennen, die DDE unterstützen keine systeminterne Konstanten in DDE-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e0d11-135">However, applications that support DDE don't recognize intrinsic constants in DDE operations.</span></span> <span data-ttu-id="e0d11-136">Darüber hinaus Zeichenfolgenargumente müssen in Anführungszeichen eingeschlossen werden (""), wenn die Zeichenfolge ein Komma enthält.</span><span class="sxs-lookup"><span data-stu-id="e0d11-136">Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma.</span></span> <span data-ttu-id="e0d11-137">Anderenfalls sind Anführungszeichen nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e0d11-137">Otherwise, quotation marks aren't required.</span></span></P>



<span data-ttu-id="e0d11-138">Die Client-Anwendung können Sie die **DDERequest** -Funktion Textdaten aus der Serveranwendung über einen geöffneten DDE-Kanal verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-138">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="e0d11-139">Oder der Client kann die Anweisung **DDEPoke** zum Senden von Daten an die Serveranwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-139">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="e0d11-140">Sobald die Datenübertragung abgeschlossen ist, kann der Client die Anweisung **DDETerminate** zum Schließen des DDE-Kanals oder der **DDETerminateAll** -Anweisung zum Schließen aller geöffneten Kanäle verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-140">Once the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e0d11-141">Wenn die Clientanwendung empfangen von Daten über einen DDE-Kanal beendet wurde, sollte es den Kanal um Speicherressourcen zu sparen schließen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-141">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span></P>


=======
- <span data-ttu-id="e0d11-142">Das Thema "System"</span><span class="sxs-lookup"><span data-stu-id="e0d11-142">The System topic</span></span>

- <span data-ttu-id="e0d11-143">Der Name einer Datenbank (Thema*Datenbank* )</span><span class="sxs-lookup"><span data-stu-id="e0d11-143">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="e0d11-144">Der Name einer Tabelle (Thema*Tabellenname* )</span><span class="sxs-lookup"><span data-stu-id="e0d11-144">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="e0d11-145">Der Name einer Abfrage (Thema*Abfragename* )</span><span class="sxs-lookup"><span data-stu-id="e0d11-145">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="e0d11-146">Eine Microsoft Access SQL-Zeichenfolge (Thema*SQLZeichenfolge* )</span><span class="sxs-lookup"><span data-stu-id="e0d11-146">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="e0d11-147">Nachdem Sie eine DDE-Verbindung hergestellt haben, können Sie die Anweisung **DDEExecute** , einen Befehl vom Client an die Server-Anwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-147">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="e0d11-148">Wenn als DDE-Server verwendet wird, erkennt Microsoft Access die folgenden Befehle als gültig:</span><span class="sxs-lookup"><span data-stu-id="e0d11-148">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="e0d11-149">Der Name eines Makros in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e0d11-149">The name of a macro in the current database.</span></span>

- <span data-ttu-id="e0d11-150">Alle Aktionen, die Sie in Visual Basic können mithilfe der Methoden des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e0d11-150">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="e0d11-151">Die OpenDatabase und SchließenDatenbank-Aktionen, die nur für DDE-Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-151">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations.</span></span> <span data-ttu-id="e0d11-152">(Ein Beispiel dafür, wie Sie diese Aktionen verwenden, finden Sie weiter unten in diesem Thema.)</span><span class="sxs-lookup"><span data-stu-id="e0d11-152">(For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="e0d11-153">Wenn Sie eine Makroaktion als Anweisung **DDEExecute** angeben, die Aktion und Argumenten führen Sie die Syntax der **DoCmd** -Objekt und müssen in Klammern ([]) eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-153">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]).</span></span> <span data-ttu-id="e0d11-154">Allerdings erkennen, die DDE unterstützen keine systeminterne Konstanten in DDE-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e0d11-154">However, applications that support DDE don't recognize intrinsic constants in DDE operations.</span></span> <span data-ttu-id="e0d11-155">Darüber hinaus Zeichenfolgenargumente müssen in Anführungszeichen eingeschlossen werden (""), wenn die Zeichenfolge ein Komma enthält.</span><span class="sxs-lookup"><span data-stu-id="e0d11-155">Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma.</span></span> <span data-ttu-id="e0d11-156">Anderenfalls sind Anführungszeichen nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e0d11-156">Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="e0d11-157">Die Client-Anwendung können Sie die **DDERequest** -Funktion Textdaten aus der Serveranwendung über einen geöffneten DDE-Kanal verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-157">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="e0d11-158">Oder der Client kann die Anweisung **DDEPoke** zum Senden von Daten an die Serveranwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-158">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="e0d11-159">Nachdem die Datenübertragung abgeschlossen ist, kann der Client die Anweisung **DDETerminate** zum Schließen des DDE-Kanals oder der **DDETerminateAll** -Anweisung zum Schließen aller offenen Kanäle verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-159">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="e0d11-160">Wenn die Clientanwendung empfangen von Daten über einen DDE-Kanal beendet wurde, sollte es den Kanal um Speicherressourcen zu sparen schließen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-160">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>
>>>>>>> <span data-ttu-id="e0d11-161">master</span><span class="sxs-lookup"><span data-stu-id="e0d11-161">master</span></span>

<span data-ttu-id="e0d11-162">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Microsoft Word-Prozedur mit Visual Basic erstellen, die Microsoft Access als DDE-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0d11-162">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server.</span></span> <span data-ttu-id="e0d11-163">(Für das Beispiel funktioniert, muss Microsoft Access ausgeführt werden.)</span><span class="sxs-lookup"><span data-stu-id="e0d11-163">(For this example to work, Microsoft Access must be running.)</span></span>

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

<a name="-head"></a><span data-ttu-id="e0d11-164"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e0d11-164"><<<<<<< HEAD</span></span>
=======
<br/>

>>>>>>> <span data-ttu-id="e0d11-165">Master-Shape, in den folgenden Abschnitten finden Sie Informationen zu den gültigen DDE-Themen, die von Microsoft Access unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0d11-165">master The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="e0d11-166">Das Thema "System"</span><span class="sxs-lookup"><span data-stu-id="e0d11-166">The System topic</span></span>

<span data-ttu-id="e0d11-167"><<<<<<< Das HEAD-System Thema befindet sich standard für alle Microsoft Windows-basierten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-167"><<<<<<< HEAD The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="e0d11-168">Es liefert Informationen zu den anderen Themen, die von der Anwendung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0d11-168">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="e0d11-169">Zugriff auf diese Informationen muss Code rufen Sie zunächst die **DDEInitiate** -Funktion mit als Argument *Thema* , und klicken Sie dann die **DDERequest** -Anweisung mit einer der folgenden Angaben für das Argument *Element* ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-169">To access this information, your code must first call the **DDEInitiate** function with as the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>
<span data-ttu-id="e0d11-170">=== Das Systemthema befindet sich standard für alle Microsoft Windows-basierten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-170">======= The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="e0d11-171">Es liefert Informationen zu den anderen Themen, die von der Anwendung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0d11-171">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="e0d11-172">Zugriff auf diese Informationen muss Code rufen Sie zunächst die **DDEInitiate** -Funktion mit dem Argument *Thema* , und klicken Sie dann die **DDERequest** -Anweisung mit einer der folgenden Angaben für das Argument *Element* ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-172">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>
>>>>>>> <span data-ttu-id="e0d11-173">master</span><span class="sxs-lookup"><span data-stu-id="e0d11-173">master</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0d11-174">Element</span><span class="sxs-lookup"><span data-stu-id="e0d11-174">Item</span></span></p></th>
<th><p><span data-ttu-id="e0d11-175">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e0d11-175">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-176">"SysItems" verwenden</span><span class="sxs-lookup"><span data-stu-id="e0d11-176">SysItems</span></span></p></td>
<td><p><span data-ttu-id="e0d11-177">Eine Liste der Elemente, die von dem Thema "System" in Microsoft Access unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0d11-177">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-178">Formate</span><span class="sxs-lookup"><span data-stu-id="e0d11-178">Formats</span></span></p></td>
<td><p><span data-ttu-id="e0d11-179">Eine Liste der Formate können Microsoft Access in die Zwischenablage kopieren.</span><span class="sxs-lookup"><span data-stu-id="e0d11-179">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-180">Status</span><span class="sxs-lookup"><span data-stu-id="e0d11-180">Status</span></span></p></td>
<td><p><span data-ttu-id="e0d11-181">&quot;Ausgelastet&quot; oder &quot;bereit&quot;.</span><span class="sxs-lookup"><span data-stu-id="e0d11-181">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-182">Topics</span><span class="sxs-lookup"><span data-stu-id="e0d11-182">Topics</span></span></p></td>
<td><p><span data-ttu-id="e0d11-183">Eine Liste aller geöffneten Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="e0d11-183">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="e0d11-184"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e0d11-184"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="e0d11-185">master</span><span class="sxs-lookup"><span data-stu-id="e0d11-185">master</span></span>

<span data-ttu-id="e0d11-186">Das folgende Beispiel veranschaulicht die Verwendung der Funktionen **DDEInitiate** und **DDERequest** mit dem Thema System:</span><span class="sxs-lookup"><span data-stu-id="e0d11-186">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

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

## <a name="the-database-topic"></a><span data-ttu-id="e0d11-187">Das Thema Datenbank</span><span class="sxs-lookup"><span data-stu-id="e0d11-187">The database topic</span></span>

<span data-ttu-id="e0d11-188">Das Thema *Datenbank* ist der Dateiname einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e0d11-188">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="e0d11-189">Sie können entweder nur den Namen der (Nordwind) oder den Pfad der Erweiterung eingeben (C:\\Access\\Beispiele\\Nordwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="e0d11-189">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="e0d11-190">Nach dem start einer DDE-Verbindung mit der Datenbank können Sie eine Liste der Objekte in der Datenbank anfordern.</span><span class="sxs-lookup"><span data-stu-id="e0d11-190">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

<span data-ttu-id="e0d11-191"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e0d11-191"><<<<<<< HEAD</span></span>

> [!NOTE]
> <P><span data-ttu-id="e0d11-192">Sie können keine DDE verwenden, um Microsoft Access-Arbeitsgruppen-Informationsdatei abzufragen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-192">You can't use DDE to query the Microsoft Access workgroup information file.</span></span></P>


=======
> [!NOTE]
> <span data-ttu-id="e0d11-193">Sie können keine DDE verwenden, um Microsoft Access-Arbeitsgruppen-Informationsdatei abzufragen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-193">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>
>>>>>>> <span data-ttu-id="e0d11-194">master</span><span class="sxs-lookup"><span data-stu-id="e0d11-194">master</span></span>

<span data-ttu-id="e0d11-195">Das Thema *Datenbank* unterstützt die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="e0d11-195">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0d11-196">Element</span><span class="sxs-lookup"><span data-stu-id="e0d11-196">Item</span></span></p></th>
<th><p><span data-ttu-id="e0d11-197">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e0d11-197">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-198">TableList</span><span class="sxs-lookup"><span data-stu-id="e0d11-198">TableList</span></span></p></td>
<span data-ttu-id="e0d11-199"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e0d11-199"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="e0d11-200">Eine Liste der Tabellen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-200">A list of tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-201">QueryList</span><span class="sxs-lookup"><span data-stu-id="e0d11-201">QueryList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-202">Eine Liste von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-202">A list of queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-203">FormList</span><span class="sxs-lookup"><span data-stu-id="e0d11-203">FormList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-204">Eine Liste von Formularen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-204">A list of forms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-205">ReportList</span><span class="sxs-lookup"><span data-stu-id="e0d11-205">ReportList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-206">Eine Liste der Berichte.</span><span class="sxs-lookup"><span data-stu-id="e0d11-206">A list of reports.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-207">MacroList</span><span class="sxs-lookup"><span data-stu-id="e0d11-207">MacroList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-208">Eine Liste mit Makros.</span><span class="sxs-lookup"><span data-stu-id="e0d11-208">A list of macros.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-209">ModuleList</span><span class="sxs-lookup"><span data-stu-id="e0d11-209">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-210">Eine Liste von Modulen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-210">A list of modules.</span></span></p></td>
=======
<td><p><span data-ttu-id="e0d11-211">Eine Liste der Tabellen</span><span class="sxs-lookup"><span data-stu-id="e0d11-211">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-212">QueryList</span><span class="sxs-lookup"><span data-stu-id="e0d11-212">QueryList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-213">Eine Liste von Abfragen</span><span class="sxs-lookup"><span data-stu-id="e0d11-213">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-214">FormList</span><span class="sxs-lookup"><span data-stu-id="e0d11-214">FormList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-215">Eine Liste von Formularen</span><span class="sxs-lookup"><span data-stu-id="e0d11-215">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-216">ReportList</span><span class="sxs-lookup"><span data-stu-id="e0d11-216">ReportList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-217">Eine Liste der Berichte</span><span class="sxs-lookup"><span data-stu-id="e0d11-217">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-218">MacroList</span><span class="sxs-lookup"><span data-stu-id="e0d11-218">MacroList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-219">Eine Liste mit Makros</span><span class="sxs-lookup"><span data-stu-id="e0d11-219">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-220">ModuleList</span><span class="sxs-lookup"><span data-stu-id="e0d11-220">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-221">Eine Liste der Module</span><span class="sxs-lookup"><span data-stu-id="e0d11-221">A list of modules</span></span></p></td><span data-ttu-id="e0d11-222">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="e0d11-222">
>>>>>>> master</span></span>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-223">ViewList</span><span class="sxs-lookup"><span data-stu-id="e0d11-223">ViewList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-224">Eine Liste der Ansichten</span><span class="sxs-lookup"><span data-stu-id="e0d11-224">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-225">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="e0d11-225">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-226">Eine Liste von gespeicherten Prozeduren</span><span class="sxs-lookup"><span data-stu-id="e0d11-226">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-227">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="e0d11-227">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="e0d11-228">Eine Liste der Datenbankdiagramme</span><span class="sxs-lookup"><span data-stu-id="e0d11-228">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="e0d11-229"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e0d11-229"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="e0d11-230">master</span><span class="sxs-lookup"><span data-stu-id="e0d11-230">master</span></span>

<span data-ttu-id="e0d11-231">Das folgende Beispiel zeigt, wie Sie das Formular Personal in der Northwind-Beispieldatenbank aus einer Visual Basic-Prozedur öffnen können:</span><span class="sxs-lookup"><span data-stu-id="e0d11-231">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

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

## <a name="the-table-topic"></a><span data-ttu-id="e0d11-232">Das Thema Tabelle</span><span class="sxs-lookup"><span data-stu-id="e0d11-232">The TABLE topic</span></span>

<span data-ttu-id="e0d11-233">In diesen Themen verwenden Sie die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="e0d11-233">These topics use the following syntax:</span></span>

<span data-ttu-id="e0d11-234">_Databasename_ ; **Tabelle** _TableName_</span><span class="sxs-lookup"><span data-stu-id="e0d11-234">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="e0d11-235">_Databasename_ ; **Abfrage** _Abfragename_</span><span class="sxs-lookup"><span data-stu-id="e0d11-235">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="e0d11-236">_Databasename_ ; **SQL** [ _Sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="e0d11-236">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0d11-237">Teil</span><span class="sxs-lookup"><span data-stu-id="e0d11-237">Part</span></span></p></th>
<th><p><span data-ttu-id="e0d11-238">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0d11-238">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-239"><em>Datenbankname</em></span><span class="sxs-lookup"><span data-stu-id="e0d11-239"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="e0d11-240">Der Name der Datenbank, die die Tabelle oder Abfrage in ist oder, die die SQL-Anweisung betrifft, gefolgt von einem Semikolon (;).</span><span class="sxs-lookup"><span data-stu-id="e0d11-240">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;).</span></span> <span data-ttu-id="e0d11-241">Der Name der Datenbank kann nur den Namen der (Nordwind) oder der vollständige Pfad und MDB-Erweiterung (C:\Access\Samples\Northwind.mdb) sein.</span><span class="sxs-lookup"><span data-stu-id="e0d11-241">The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-242"><em>TableName</em></span><span class="sxs-lookup"><span data-stu-id="e0d11-242"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="e0d11-243">Der Name einer vorhandenen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e0d11-243">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-244"><em>Abfragename</em></span><span class="sxs-lookup"><span data-stu-id="e0d11-244"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="e0d11-245">Der Name einer vorhandenen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="e0d11-245">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-246"><em>SqlString</em></span><span class="sxs-lookup"><span data-stu-id="e0d11-246"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="e0d11-247">Eine gültige SQL­Anweisung bis zu 256 Zeichen lang sein, mit einem Semikolon enden.</span><span class="sxs-lookup"><span data-stu-id="e0d11-247">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="e0d11-248">Um mehr als 256 Zeichen austauschen möchten, geben Sie dieses Argument und stattdessen verwenden Sie aufeinander folgenden <strong>DDEPoke</strong> -Anweisungen zum Erstellen einer SQL-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="e0d11-248">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="e0d11-249">Der folgenden Visual Basic-Code wird beispielsweise die Anweisung <strong>DDEPoke</strong> So erstellen eine SQL-Anweisung, und fordern Sie dann die Ergebnisse der Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0d11-249">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="e0d11-250">In der folgenden Tabelle sind die gültigen Elemente für die Tabelle *Tabellenname*, QUERY *Abfragename*und SQL *SQLZeichenfolge* Themen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-250">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0d11-251">Element</span><span class="sxs-lookup"><span data-stu-id="e0d11-251">Item</span></span></p></th>
<th><p><span data-ttu-id="e0d11-252">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e0d11-252">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-253">Alle</span><span class="sxs-lookup"><span data-stu-id="e0d11-253">All</span></span></p></td>
<td><p><span data-ttu-id="e0d11-254">Die Daten in der Tabelle, einschließlich Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-254">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-255">Daten</span><span class="sxs-lookup"><span data-stu-id="e0d11-255">Data</span></span></p></td>
<td><p><span data-ttu-id="e0d11-256">Alle Zeilen mit Daten, ohne Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-256">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-257">FieldNames</span><span class="sxs-lookup"><span data-stu-id="e0d11-257">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="e0d11-258">Eine einzeilige Liste von Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-258">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-259">FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="e0d11-259">FieldNames;T</span></span></p></td>
<span data-ttu-id="e0d11-260"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e0d11-260"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="e0d11-261">Eine zwei Zeilen Liste von Feldnamen (erste Zeile) und deren Datentypen (zweite Zeile).</span><span class="sxs-lookup"><span data-stu-id="e0d11-261">A two-row list of field names (first row) and their data types (second row).</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-262">Dies sind die zurückgegebenen Werte und die Datentypen, die sie darstellen:</span><span class="sxs-lookup"><span data-stu-id="e0d11-262">These are the values returned and the data types they represent:</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-263"><b>Wert</b></span><span class="sxs-lookup"><span data-stu-id="e0d11-263"><b>Value</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-264">0</span><span class="sxs-lookup"><span data-stu-id="e0d11-264">0</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-265">1</span><span class="sxs-lookup"><span data-stu-id="e0d11-265">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-266">2</span><span class="sxs-lookup"><span data-stu-id="e0d11-266">2</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-267">3</span><span class="sxs-lookup"><span data-stu-id="e0d11-267">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-268">4</span><span class="sxs-lookup"><span data-stu-id="e0d11-268">4</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-269">5</span><span class="sxs-lookup"><span data-stu-id="e0d11-269">5</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-270">6</span><span class="sxs-lookup"><span data-stu-id="e0d11-270">6</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-271">7</span><span class="sxs-lookup"><span data-stu-id="e0d11-271">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-272">8</span><span class="sxs-lookup"><span data-stu-id="e0d11-272">8</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-273">9</span><span class="sxs-lookup"><span data-stu-id="e0d11-273">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-274">10</span><span class="sxs-lookup"><span data-stu-id="e0d11-274">10</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-275">11</span><span class="sxs-lookup"><span data-stu-id="e0d11-275">11</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e0d11-276">12</span><span class="sxs-lookup"><span data-stu-id="e0d11-276">12</span></span></p></td>
=======
<td><p><span data-ttu-id="e0d11-277">Eine zwei Zeilen Liste von Feldnamen (erste Zeile) und deren Datentypen (zweite Zeile).</span><span class="sxs-lookup"><span data-stu-id="e0d11-277">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="e0d11-278">Dies sind die zurückgegebenen Werte:</span><span class="sxs-lookup"><span data-stu-id="e0d11-278">These are the values returned:</span></span></p>
<p><span data-ttu-id="e0d11-279">Wert</span><span class="sxs-lookup"><span data-stu-id="e0d11-279">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="e0d11-280">0</span><span class="sxs-lookup"><span data-stu-id="e0d11-280">0</span></span></li>
<li><span data-ttu-id="e0d11-281">1</span><span class="sxs-lookup"><span data-stu-id="e0d11-281">1</span></span></li>
<li><span data-ttu-id="e0d11-282">2</span><span class="sxs-lookup"><span data-stu-id="e0d11-282">2</span></span></li>
<li><span data-ttu-id="e0d11-283">3</span><span class="sxs-lookup"><span data-stu-id="e0d11-283">3</span></span></li>
<li><span data-ttu-id="e0d11-284">4</span><span class="sxs-lookup"><span data-stu-id="e0d11-284">4</span></span></li>
<li><span data-ttu-id="e0d11-285">5</span><span class="sxs-lookup"><span data-stu-id="e0d11-285">5</span></span></li>
<li><span data-ttu-id="e0d11-286">6</span><span class="sxs-lookup"><span data-stu-id="e0d11-286">6</span></span></li>
<li><span data-ttu-id="e0d11-287">7</span><span class="sxs-lookup"><span data-stu-id="e0d11-287">7</span></span></li>
<li><span data-ttu-id="e0d11-288">8</span><span class="sxs-lookup"><span data-stu-id="e0d11-288">8</span></span></li>
<li><span data-ttu-id="e0d11-289">9</span><span class="sxs-lookup"><span data-stu-id="e0d11-289">9</span></span></li>
<li><span data-ttu-id="e0d11-290">10</span><span class="sxs-lookup"><span data-stu-id="e0d11-290">10</span></span></li>
<li><span data-ttu-id="e0d11-291">11</span><span class="sxs-lookup"><span data-stu-id="e0d11-291">11</span></span></li>
<li><span data-ttu-id="e0d11-292">12</span><span class="sxs-lookup"><span data-stu-id="e0d11-292">12</span></span></li>
</ul>
</p>
</td><span data-ttu-id="e0d11-293">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="e0d11-293">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-294">NextRow</span><span class="sxs-lookup"><span data-stu-id="e0d11-294">NextRow</span></span></p></td>
<td><p><span data-ttu-id="e0d11-295">Die Daten in der nächsten Zeile in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="e0d11-295">The data in the next row in the table or query.</span></span> <span data-ttu-id="e0d11-296">Wenn Sie einen Kanal öffnen, gibt NextRow die Daten in der ersten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e0d11-296">When you open a channel, NextRow returns the data in the first row.</span></span> <span data-ttu-id="e0d11-297">Wenn die aktuelle Zeile der letzte Datensatz ist und Ausführung von NextRow, schlägt die Anforderung fehl.</span><span class="sxs-lookup"><span data-stu-id="e0d11-297">If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-298">Fehl</span><span class="sxs-lookup"><span data-stu-id="e0d11-298">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="e0d11-299">Die Daten in der vorherigen Zeile in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="e0d11-299">The data in the previous row in the table or query.</span></span> <span data-ttu-id="e0d11-300">Wenn fehl die erste Anforderung über einen neuen Kanal ist, werden die Daten in der letzten Zeile der Tabelle oder Abfrage zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0d11-300">If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned.</span></span> <span data-ttu-id="e0d11-301">Wenn der erste Datensatz der aktuelle Zeile ist, schlägt die Anforderung fehl.</span><span class="sxs-lookup"><span data-stu-id="e0d11-301">If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-302">FirstRow</span><span class="sxs-lookup"><span data-stu-id="e0d11-302">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="e0d11-303">Die Daten in der ersten Zeile der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="e0d11-303">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-304">LastRow</span><span class="sxs-lookup"><span data-stu-id="e0d11-304">LastRow</span></span></p></td>
<td><p><span data-ttu-id="e0d11-305">Die Daten in der letzten Zeile der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="e0d11-305">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-306">FieldCount</span><span class="sxs-lookup"><span data-stu-id="e0d11-306">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="e0d11-307">Die Anzahl der Felder in der Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="e0d11-307">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d11-308">SQLText</span><span class="sxs-lookup"><span data-stu-id="e0d11-308">SQLText</span></span></p></td>
<td><p><span data-ttu-id="e0d11-309">Eine SQL-Anweisung, die die Tabelle oder Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0d11-309">An SQL statement representing the table or query.</span></span> <span data-ttu-id="e0d11-310">Für Tabellen, gibt dieses Element eine SQL-Anweisung in der Form &quot;auswählen `*` FROM <em>Tabelle</em>; &quot;.</span><span class="sxs-lookup"><span data-stu-id="e0d11-310">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d11-311">SQLText; <em>n</em></span><span class="sxs-lookup"><span data-stu-id="e0d11-311">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="e0d11-312">Eine SQL­Anweisung in <em>n</em>-Segmenten für eine Tabelle oder Abfrage, wobei <em>n</em> eine ganze Zahl bis zu 256 ist Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e0d11-312">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="e0d11-313">Nehmen wir beispielsweise bei eine Abfrage wird durch die folgende SQL-Anweisung dargestellt: das Element &quot;SQLText; 7&quot; gibt die folgenden Abschnitte Tabstopp-getrennt: das Element &quot;SQLText; 7&quot; gibt die folgenden Abschnitte Tabstopp-getrennt:</span><span class="sxs-lookup"><span data-stu-id="e0d11-313">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="e0d11-314"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e0d11-314"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="e0d11-315">master</span><span class="sxs-lookup"><span data-stu-id="e0d11-315">master</span></span>

<span data-ttu-id="e0d11-316">Das folgende Beispiel zeigt, wie Sie DDE in einer Visual Basic-Prozedur das Abrufen von Daten aus einer Tabelle in der Northwind-Beispieldatenbank verwenden und diese Daten in eine Textdatei einfügen:</span><span class="sxs-lookup"><span data-stu-id="e0d11-316">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

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
