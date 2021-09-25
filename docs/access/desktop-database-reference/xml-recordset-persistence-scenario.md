---
title: Speicherszenario für XML-Recordset
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 99f8216c64b24328140aa5a0cc1b117c3008aee1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593159"
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

1. Erstellen Sie ein virtuelles IIS-Verzeichnis namens **XMLPersist** mit Skriptberechtigungen. 

2. Erstellen Sie zwei neue Textdateien in dem Ordner, auf den das virtuelle Verzeichnis verweist, eine mit dem Namen **XMLResponse.asp** und die andere mit dem Namen **Default.htm.**


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

2. Ändern Sie unbedingt den Wert des Datenquellenparameters in strCon in den Namen Ihres Microsoft SQL Server Computers.

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

   Beachten Sie, dass das ASP **Response-Objekt** als Ziel für die **Recordset** [Save-Methode](save-method-ado.md) angegeben ist. Das Ziel der **Save**-Methode kann jedes beliebige Objekt sein, das die **IStream**-Schnittstelle unterstützt, z. B. ein ADO-Objekt [Stream](stream-object-ado.md) oder ein Dateiname, der den vollständigen Pfad einschließt, unter dem das **Recordset**-Objekt gespeichert wird.

2. Save and close XMLResponse.asp before going to the next step. Kopieren Sie außerdem die Datei "adovbs.inc" aus dem Ordner "C: \\ Program Files Common Files System \\ \\ \\ Ado" in denselben Ordner, in dem Sie die Datei "XMLResponse.asp" haben.

## <a name="step-4-receive-and-display-the-data"></a>Schritt 4: Empfangen und Anzeigen der Daten

In diesem Schritt erstellen Sie eine HTML-Datei mit einem eingebetteten [RDS. DataControl-Objekt,](datacontrol-object-rds.md) das auf die Datei XMLResponse.asp zeigt, um das **Recordset** abzurufen. 

1. Öffnen Sie default.htm mit einem Text-Editor, z. B. Windows Editor, und fügen Sie den folgenden Code hinzu. Ersetzen Sie "sqlserver" in der URL durch den Namen Ihres Servercomputers.

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

2. Schließen Sie die default.htm Datei, und speichern Sie sie in demselben Ordner, in dem Sie XMLResponse.asp gespeichert haben. 

3. Öffnen Sie mit Internet Explorer 4.0 oder höher die URL, `https://<sqlserver>/XMLPersist/default.htm` und beobachten Sie die Ergebnisse. Die Daten werden in einer gebundenen DHTML-Tabelle angezeigt. 

4. Öffnen Sie nun die `https://<sqlserver>/XMLPersist/XMLResponse.asp` URL, und beobachten Sie die Ergebnisse. Der XML-Code wird angezeigt.




