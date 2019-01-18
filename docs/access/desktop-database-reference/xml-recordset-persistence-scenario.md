---
title: Speicherszenario für XML-Recordset
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bae48f3e9b2b5c3967b955c41ba01c634546164
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711532"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="592e0-102">Speicherszenario für XML-Recordset</span><span class="sxs-lookup"><span data-stu-id="592e0-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="592e0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="592e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="592e0-104">In diesem Szenario erstellen Sie eine ASP-Anwendung (Active Server Pages), die den Inhalt eines **Recordset** -Objekts direkt in das **ASP-Response** -Objekt speichert.</span><span class="sxs-lookup"><span data-stu-id="592e0-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="592e0-105">[!HINWEIS] Für dieses Szenario muss Internetinformationsdienste (IIS) 5.0 oder höher installiert sein.</span><span class="sxs-lookup"><span data-stu-id="592e0-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="592e0-106">Das zurückgegebene **Recordset** -Objekt wird unter Verwendung eines [RDS.DataControl](datacontrol-object-rds.md)-Objekts in Internet Explorer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="592e0-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="592e0-107">Die folgenden Schritte sind für dieses Szenario erforderlich:</span><span class="sxs-lookup"><span data-stu-id="592e0-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="592e0-108">Einrichten der Anwendung</span><span class="sxs-lookup"><span data-stu-id="592e0-108">Set up the application.</span></span>
2.  <span data-ttu-id="592e0-109">Abrufen der Daten</span><span class="sxs-lookup"><span data-stu-id="592e0-109">Get the data.</span></span>
3.  <span data-ttu-id="592e0-110">Senden der Daten</span><span class="sxs-lookup"><span data-stu-id="592e0-110">Send the data.</span></span>
4.  <span data-ttu-id="592e0-111">Empfangen und Anzeigen der Daten</span><span class="sxs-lookup"><span data-stu-id="592e0-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="592e0-112">Schritt 1: Einrichten der Anwendung</span><span class="sxs-lookup"><span data-stu-id="592e0-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="592e0-113">Erstellen Sie ein virtuelles IIS-Verzeichnis mit dem Namen **XMLPersist** und Skriptberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="592e0-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="592e0-114">Erstellen Sie zwei neue Textdateien im Ordner, den das virtuelle Verzeichnis verweist, eine benannte **XMLResponse.asp**und die andere mit dem Namen **Default.htm**.</span><span class="sxs-lookup"><span data-stu-id="592e0-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="592e0-115">Schritt 2: Abrufen der Daten</span><span class="sxs-lookup"><span data-stu-id="592e0-115">Step 2: Get the data</span></span>

<span data-ttu-id="592e0-116">In diesem Schritt schreiben Sie den Code zum Öffnen eines ADO- **Recordset-Objekt** und Vorbereitung der es an den Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="592e0-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="592e0-117">Öffnen Sie die Datei XMLResponse.asp mit einem Text-Editor wie Windows Editor ein, und fügen Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="592e0-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

   ```vb 
        
        <%@ language="VBScript" %> 
        
        <!-- #include file='adovbs.inc' --> 
        
        <% 
        Dim strSQL, strCon 
        Dim adoRec  
        Dim adoCon  
        Dim xmlDoc  
        
        ' You will need to change "slqServer" below to the name of the SQL  
        ' server machine to which you want to connect. 
        strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
        Set adoCon = server.createObject("ADODB.Connection") 
        adoCon.Open strCon 
        
        strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
        Set adoRec = Server.CreateObject("ADODB.Recordset") 
        adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
   ```

2. <span data-ttu-id="592e0-118">Achten Sie darauf, dass Sie den Wert des Parameters Datenquelle im StrCon auf den Namen des Microsoft SQL Server-Computers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="592e0-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="592e0-119">Lassen Sie die Datei geöffnet, und wechseln Sie zum nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="592e0-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="592e0-120">Schritt 3: Senden der Daten</span><span class="sxs-lookup"><span data-stu-id="592e0-120">Step 3: Send the data</span></span>

<span data-ttu-id="592e0-121">Nachdem Sie ein **Recordset-Objekt**haben, müssen Sie durch Speichern als XML für das ASP- **Response** -Objekt an den Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="592e0-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="592e0-122">Fügen Sie den folgenden Code am Ende der XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="592e0-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

   ```vb 
    
    Response.ContentType = "text/xml" 
    Response.Expires = 0 
    Response.Buffer = False 
    
    
    Response.Write "<?xml version='1.0'?>" & vbNewLine 
    adoRec.save Response, adPersistXML 
    adoRec.Close 
    Set adoRec=Nothing 
    %> 
   ```

   <span data-ttu-id="592e0-123">Beachten Sie, dass das ASP- **Response** -Objekt als Ziel für die **Recordset-Objekt** [Speichern](save-method-ado.md) -Methode angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="592e0-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="592e0-124">Das Ziel des **Save** -Methode kann jedes Objekt sein, die unterstützt die **IStream** -Schnittstelle, wie ein ADO- [Stream](stream-object-ado.md) -Objekt oder einen Dateinamen ein, der den vollständigen Pfad enthält, wird das **Recordset-Objekt** gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="592e0-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="592e0-125">Speichern Sie und schließen Sie XMLResponse.asp, bevor Sie mit dem nächsten Schritt fortfahren.</span><span class="sxs-lookup"><span data-stu-id="592e0-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="592e0-126">Kopieren Sie die Datei adovbs.inc-Datei auch von C:\\Program Files\\gemeinsame Dateien\\System\\Ado-Ordner im gleichen Ordner, in dem Sie die Datei XMLResponse.asp verfügen.</span><span class="sxs-lookup"><span data-stu-id="592e0-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="592e0-127">Schritt 4: Empfangen und Anzeigen der Daten</span><span class="sxs-lookup"><span data-stu-id="592e0-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="592e0-128">In diesem Schritt erstellen Sie eine HTML-Datei mit einer eingebetteten [RDS. DataControl](datacontrol-object-rds.md) -Objekt, das auf die Datei XMLResponse.asp abzurufenden das **Recordset-Objekt**zeigt.</span><span class="sxs-lookup"><span data-stu-id="592e0-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="592e0-129">Öffnen Sie default.htm mit einem Text-Editor wie Windows Editor ein, und fügen Sie den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="592e0-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="592e0-130">Ersetzen Sie "Sqlserver" in der URL durch den Namen des Server-Computers ein.</span><span class="sxs-lookup"><span data-stu-id="592e0-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

   ```html 
    
    <HTML> 
    <HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
    <BODY> 
    
    <TABLE DATASRC="#RDC1" border="1"> 
    <TR> 
    <TD><SPAN DATAFLD="title"></SPAN></TD> 
    <TD><SPAN DATAFLD="price"></SPAN></TD> 
    </TR> 
    </TABLE> 

    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
    <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
    </OBJECT> 
    
    </BODY> 
    </HTML> 
   ```

2. <span data-ttu-id="592e0-131">Schließen Sie die Datei ' default.htm ', und speichern Sie sie im gleichen Ordner, in dem Sie XMLResponse.asp gespeichert.</span><span class="sxs-lookup"><span data-stu-id="592e0-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="592e0-132">Verwenden von Internet Explorer 4.0 oder höher, öffnen Sie die URL `https://<sqlserver>/XMLPersist/default.htm` und zeigen die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="592e0-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="592e0-133">Die Daten werden in einer gebundenen DHTML-Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="592e0-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="592e0-134">Öffnen Sie nun die URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` und zeigen die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="592e0-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="592e0-135">Der XML-Code wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="592e0-135">The XML is displayed.</span></span>




