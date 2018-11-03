---
title: Speicherszenario für XML-Recordset
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4840b59f8f145b17b45a9732443d3f844b336868
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945488"
---
# <a name="xml-recordset-persistence-scenario"></a>Speicherszenario für XML-Recordset

**Betrifft**: Access 2013, Office 2013

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

1. Erstellen Sie ein virtuelles IIS-Verzeichnis mit dem Namen **XMLPersist** und Skriptberechtigungen. 

2. Erstellen Sie zwei neue Textdateien im Ordner, den das virtuelle Verzeichnis verweist, eine benannte **XMLResponse.asp**und die andere mit dem Namen **Default.htm**.


## <a name="step-2-get-the-data"></a>Schritt 2: Abrufen der Daten

In diesem Schritt schreiben Sie den Code zum Öffnen eines ADO- **Recordset-Objekt** und Vorbereitung der es an den Client gesendet. 

1. Öffnen Sie die Datei XMLResponse.asp mit einem Text-Editor wie Windows Editor ein, und fügen Sie den folgenden Code:

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

2. Achten Sie darauf, dass Sie den Wert des Parameters Datenquelle im StrCon auf den Namen des Microsoft SQL Server-Computers zu ändern.

3. Lassen Sie die Datei geöffnet, und wechseln Sie zum nächsten Schritt.

## <a name="step-3-send-the-data"></a>Schritt 3: Senden der Daten

Nachdem Sie ein **Recordset-Objekt**haben, müssen Sie durch Speichern als XML für das ASP- **Response** -Objekt an den Client gesendet. 

1. Fügen Sie den folgenden Code am Ende der XMLResponse.asp:

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

   Beachten Sie, dass das ASP- **Response** -Objekt als Ziel für die **Recordset-Objekt** [Speichern](save-method-ado.md) -Methode angegeben wird. Das Ziel des **Save** -Methode kann jedes Objekt sein, die unterstützt die **IStream** -Schnittstelle, wie ein ADO- [Stream](stream-object-ado.md) -Objekt oder einen Dateinamen ein, der den vollständigen Pfad enthält, wird das **Recordset-Objekt** gespeichert werden soll.

2. Speichern Sie und schließen Sie XMLResponse.asp, bevor Sie mit dem nächsten Schritt fortfahren. Kopieren Sie die Datei adovbs.inc-Datei auch von C:\\Program Files\\gemeinsame Dateien\\System\\Ado-Ordner im gleichen Ordner, in dem Sie die Datei XMLResponse.asp verfügen.

## <a name="step-4-receive-and-display-the-data"></a>Schritt 4: Empfangen und Anzeigen der Daten

In diesem Schritt erstellen Sie eine HTML-Datei mit einer eingebetteten [RDS. DataControl](datacontrol-object-rds.md) -Objekt, das auf die Datei XMLResponse.asp abzurufenden das **Recordset-Objekt**zeigt. 

1. Öffnen Sie default.htm mit einem Text-Editor wie Windows Editor ein, und fügen Sie den folgenden Code hinzu. Ersetzen Sie "Sqlserver" in der URL durch den Namen des Server-Computers ein.

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

2. Schließen Sie die Datei ' default.htm ', und speichern Sie sie im gleichen Ordner, in dem Sie XMLResponse.asp gespeichert. 

3. Verwenden von Internet Explorer 4.0 oder höher, öffnen Sie die URL `https://<sqlserver>/XMLPersist/default.htm` und zeigen die Ergebnisse. Die Daten werden in einer gebundenen DHTML-Tabelle angezeigt. 

4. Öffnen Sie nun die URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` und zeigen die Ergebnisse. Der XML-Code wird angezeigt.




