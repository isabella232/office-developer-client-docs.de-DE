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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302594"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="fb181-102">Speicherszenario für XML-Recordset</span><span class="sxs-lookup"><span data-stu-id="fb181-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="fb181-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb181-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb181-104">In diesem Szenario erstellen Sie eine ASP-Anwendung (Active Server Pages), die den Inhalt eines **Recordset** -Objekts direkt in das **ASP-Response** -Objekt speichert.</span><span class="sxs-lookup"><span data-stu-id="fb181-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="fb181-105">[!HINWEIS] Für dieses Szenario muss Internetinformationsdienste (IIS) 5.0 oder höher installiert sein.</span><span class="sxs-lookup"><span data-stu-id="fb181-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="fb181-106">Das zurückgegebene **Recordset** -Objekt wird unter Verwendung eines [RDS.DataControl](datacontrol-object-rds.md)-Objekts in Internet Explorer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb181-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="fb181-107">Die folgenden Schritte sind für dieses Szenario erforderlich:</span><span class="sxs-lookup"><span data-stu-id="fb181-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="fb181-108">Einrichten der Anwendung</span><span class="sxs-lookup"><span data-stu-id="fb181-108">Set up the application.</span></span>
2.  <span data-ttu-id="fb181-109">Abrufen der Daten</span><span class="sxs-lookup"><span data-stu-id="fb181-109">Get the data.</span></span>
3.  <span data-ttu-id="fb181-110">Senden der Daten</span><span class="sxs-lookup"><span data-stu-id="fb181-110">Send the data.</span></span>
4.  <span data-ttu-id="fb181-111">Empfangen und Anzeigen der Daten</span><span class="sxs-lookup"><span data-stu-id="fb181-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="fb181-112">Schritt 1: Einrichten der Anwendung</span><span class="sxs-lookup"><span data-stu-id="fb181-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="fb181-113">Erstellen Sie ein virtuelles IIS- \*\*\*\* Verzeichnis mit dem Namen XMLPersist mit Skriptberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="fb181-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="fb181-114">Erstellen Sie zwei neue Textdateien in dem Ordner, auf den das virtuelle Verzeichnis zeigt, einen mit dem Namen " **XMLResponse. ASP**" und den anderen Namen " **default. htm**".</span><span class="sxs-lookup"><span data-stu-id="fb181-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="fb181-115">Schritt 2: Abrufen der Daten</span><span class="sxs-lookup"><span data-stu-id="fb181-115">Step 2: Get the data</span></span>

<span data-ttu-id="fb181-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span><span class="sxs-lookup"><span data-stu-id="fb181-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="fb181-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span><span class="sxs-lookup"><span data-stu-id="fb181-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

2. <span data-ttu-id="fb181-118">Stellen Sie sicher, dass Sie den Wert des Parameters Datenquelle in strCon in den Namen des Microsoft SQL Server-Computers ändern.</span><span class="sxs-lookup"><span data-stu-id="fb181-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="fb181-119">Lassen Sie die Datei geöffnet, und wechseln Sie zum nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="fb181-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="fb181-120">Schritt 3: Senden der Daten</span><span class="sxs-lookup"><span data-stu-id="fb181-120">Step 3: Send the data</span></span>

<span data-ttu-id="fb181-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span><span class="sxs-lookup"><span data-stu-id="fb181-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="fb181-122">Add the following code to the bottom of XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="fb181-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

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

   <span data-ttu-id="fb181-123">Beachten Sie, dass das ASP- **Antwort** Objekt als Ziel für die \*\*\*\* [Save](save-method-ado.md) -Methode des Recordset-Objekts angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb181-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="fb181-124">Das Ziel der **Save**-Methode kann jedes beliebige Objekt sein, das die **IStream**-Schnittstelle unterstützt, z. B. ein ADO-Objekt [Stream](stream-object-ado.md) oder ein Dateiname, der den vollständigen Pfad einschließt, unter dem das **Recordset**-Objekt gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="fb181-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="fb181-125">Save and close XMLResponse.asp before going to the next step.</span><span class="sxs-lookup"><span data-stu-id="fb181-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="fb181-126">Kopieren Sie auch die Datei Datei Adovbs. Inc aus dem\\Ordner C\\: Program\\Files\\Common Files System ADO in den Ordner, in dem Sie die Datei XMLResponse. ASP haben.</span><span class="sxs-lookup"><span data-stu-id="fb181-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="fb181-127">Schritt 4: empfangen und Anzeigen der Daten</span><span class="sxs-lookup"><span data-stu-id="fb181-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="fb181-128">In diesem Schritt erstellen Sie eine HTML-Datei mit einem eingebetteten [RDS. DataControl](datacontrol-object-rds.md) -Objekt, das auf die XMLResponse. ASP-Datei zeigt, um das **Recordset**abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fb181-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="fb181-129">Öffnen Sie Default. htm mit einem Text-Editor wie Windows Notepad, und fügen Sie den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb181-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="fb181-130">Ersetzen Sie "SQLServer" in der URL durch den Namen Ihres Servercomputers.</span><span class="sxs-lookup"><span data-stu-id="fb181-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

2. <span data-ttu-id="fb181-131">Beenden Sie die Datei default. htm, und speichern Sie Sie in dem Ordner, in dem Sie xmlResponse. ASP gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="fb181-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="fb181-132">Öffnen Sie mit Internet Explorer 4,0 oder höher die URL `https://<sqlserver>/XMLPersist/default.htm` , und beobachten Sie die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="fb181-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="fb181-133">Die Daten werden in einer gebundenen DHTML-Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb181-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="fb181-134">Öffnen Sie nun die `https://<sqlserver>/XMLPersist/XMLResponse.asp` URL, und beobachten Sie die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="fb181-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="fb181-135">Der XML-Code wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb181-135">The XML is displayed.</span></span>




