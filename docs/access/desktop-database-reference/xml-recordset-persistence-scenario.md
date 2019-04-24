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
# <a name="xml-recordset-persistence-scenario"></a>Speicherszenario für XML-Recordset

**Gilt für**: Access 2013, Office 2013

In diesem Szenario erstellen Sie eine ASP-Anwendung (Active Server Pages), die den Inhalt eines **Recordset** -Objekts direkt in das **ASP-Response** -Objekt speichert.

> [!NOTE]
> [!HINWEIS] Für dieses Szenario muss Internetinformationsdienste (IIS) 5.0 oder höher installiert sein.

Das zurückgegebene **Recordset** -Objekt wird unter Verwendung eines [RDS.DataControl](datacontrol-object-rds.md)-Objekts in Internet Explorer angezeigt.

Die folgenden Schritte sind für dieses Szenario erforderlich:

1.  Einrichten der Anwendung
2.  Abrufen der Daten
3.  Senden der Daten
4.  Empfangen und Anzeigen der Daten

## <a name="step-1-set-up-the-application"></a>Schritt 1: Einrichten der Anwendung

1. Erstellen Sie ein virtuelles IIS- **** Verzeichnis mit dem Namen XMLPersist mit Skriptberechtigungen. 

2. Erstellen Sie zwei neue Textdateien in dem Ordner, auf den das virtuelle Verzeichnis zeigt, einen mit dem Namen " **XMLResponse. ASP**" und den anderen Namen " **default. htm**".


## <a name="step-2-get-the-data"></a>Schritt 2: Abrufen der Daten

In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client. 

1. Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:

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

2. Stellen Sie sicher, dass Sie den Wert des Parameters Datenquelle in strCon in den Namen des Microsoft SQL Server-Computers ändern.

3. Lassen Sie die Datei geöffnet, und wechseln Sie zum nächsten Schritt.

## <a name="step-3-send-the-data"></a>Schritt 3: Senden der Daten

Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object. 

1. Add the following code to the bottom of XMLResponse.asp:

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

   Beachten Sie, dass das ASP- **Antwort** Objekt als Ziel für die **** [Save](save-method-ado.md) -Methode des Recordset-Objekts angegeben wird. Das Ziel der **Save**-Methode kann jedes beliebige Objekt sein, das die **IStream**-Schnittstelle unterstützt, z. B. ein ADO-Objekt [Stream](stream-object-ado.md) oder ein Dateiname, der den vollständigen Pfad einschließt, unter dem das **Recordset**-Objekt gespeichert wird.

2. Save and close XMLResponse.asp before going to the next step. Kopieren Sie auch die Datei Datei Adovbs. Inc aus dem\\Ordner C\\: Program\\Files\\Common Files System ADO in den Ordner, in dem Sie die Datei XMLResponse. ASP haben.

## <a name="step-4-receive-and-display-the-data"></a>Schritt 4: empfangen und Anzeigen der Daten

In diesem Schritt erstellen Sie eine HTML-Datei mit einem eingebetteten [RDS. DataControl](datacontrol-object-rds.md) -Objekt, das auf die XMLResponse. ASP-Datei zeigt, um das **Recordset**abzurufen. 

1. Öffnen Sie Default. htm mit einem Text-Editor wie Windows Notepad, und fügen Sie den folgenden Code hinzu. Ersetzen Sie "SQLServer" in der URL durch den Namen Ihres Servercomputers.

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

2. Beenden Sie die Datei default. htm, und speichern Sie Sie in dem Ordner, in dem Sie xmlResponse. ASP gespeichert haben. 

3. Öffnen Sie mit Internet Explorer 4,0 oder höher die URL `https://<sqlserver>/XMLPersist/default.htm` , und beobachten Sie die Ergebnisse. Die Daten werden in einer gebundenen DHTML-Tabelle angezeigt. 

4. Öffnen Sie nun die `https://<sqlserver>/XMLPersist/XMLResponse.asp` URL, und beobachten Sie die Ergebnisse. Der XML-Code wird angezeigt.




