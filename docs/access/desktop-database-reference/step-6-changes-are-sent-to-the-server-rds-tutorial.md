---
title: 'Schritt 6: Senden von Änderungen an den Server (RDS-Lernprogramm)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9f75e5215e3e3d79363ab7110f7c16bcacf3cbb
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998994"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a>Schritt 6: Änderungen werden an den Server (RDS-Lernprogramm) gesendet.

**Betrifft**: Access 2013, Office 2013

Beim Bearbeiten eines **Recordset** -Objekts können alle Änderungen (d. h. hinzugefügte, geänderte oder gelöschte Zeilen) zurück an den Server gesendet werden.

[!HINWEIS] Das Standardverhalten von RDS kann implizit mit ADO-Objekten und dem Microsoft OLE DB-Anbieter für Remoting aufgerufen werden. Abfragen können **Recordsets**zurückgegeben und bearbeiteten **Recordsets** kann die Datenquelle aktualisieren. In diesem Lernprogramm wird RDS nicht mit ADO-Objekten aufgerufen, was folgendermaßen aussehen würde:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

**Teil A** 

In diesem Fall: Angenommen Sie, Sie nur die [RDS. verwendet haben DataControl](datacontrol-object-rds.md) zugeordnet und ein **Recordset** -Objekt ist jetzt die **RDS. DataControl**. Die Datenquelle wird durch die [SubmitChanges](submitchanges-method-rds.md)-Methode mit allen Änderungen am **Recordset** -Objekt aktualisiert, wenn die Eigenschaften [Server](server-property-rds.md) und [Connect](connect-property-rds.md) noch festgelegt sind.

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

**Teil B** 

Alternativ können Sie den Server mit dem [RDSServer.DataFactory](datafactory-object-rdsserver.md) -Objekt aktualisieren und eine Verbindung sowie ein **Recordset** -Objekt angeben.

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

**Dies ist das Ende des Lernprogramms.**

