---
title: 'Schritt 2: Aufrufen des Serverprogramms (RDS-Lernprogramm)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edd9f8561e6275e3b8eb33e86be745345d7c797a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475679"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a>Schritt 2: Aufrufen des Serverprogramms (RDS-Lernprogramm)


**Betrifft**: Access 2013 | Office 2013

Wenn Sie auf dem Client*proxy* eine Methode aufrufen, wird die Methode vom tatsächlichen Programm auf dem Server ausgeführt. In diesem Schritt führen Sie eine Abfrage auf dem Server durch.

**Teil A** Wenn Sie in diesem Lernprogramm [RDSServer.DataFactory](datafactory-object-rdsserver.md) verwendet haben, wäre Weise zum Ausführen dieses Schritts, verwenden Sie die [RDS. DataControl](datacontrol-object-rds.md) Objekt. Das **RDS.DataControl** -Objekt verbindet den vorherigen Schritt des Erstellens eines Proxys mit diesem Schritt des Erstellens einer Abfrage.

Geben Sie anhand der **Server**-Eigenschaft des [RDS.DataControl](server-property-rds.md) -Objekts an, wo das Serverprogramm instanziiert werden soll. Geben Sie mit der [Connect](connect-property-rds.md)-Eigenschaft die Verbindungszeichenfolge für den Zugriff auf die Datenquelle an, und geben Sie mit der [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\))-Eigenschaft den Text des Abfragebefehls an. Rufen Sie dann die [Refresh](refresh-method-rds.md)-Methode auf, sodass das Serverprogramm die Verbindung mit der Datenquelle herstellt, die in der Abfrage angegebenen Zeilen abruft und ein **Recordset** -Objekt an den Client zurückgibt.

In diesem Lernprogramm wird zwar kein **RDS.DataControl** -Objekt verwendet, es würde jedoch folgendermaßen auftreten:

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

In diesem Lernprogramm wird RDS auch nicht mit ADO-Objekten aufgerufen, was folgendermaßen aussehen würde:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

**Teil B** Die allgemeine-Methode des für diesen Schritt ist das **RDSServer.DataFactory** -Objekt, [Query](query-method-rds.md) -Methode aufrufen. In diese Methode wird anhand einer Verbindungszeichenfolge eine Verbindung mit der Datenquelle hergestellt, und mit einem Befehlstext werden die Zeilen angegeben, die aus der Datenquelle zurückgegeben werden sollen.

In diesem Lernprogramm wird die **Query** -Methode des **DataFactory** -Objekts verwendet:

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

