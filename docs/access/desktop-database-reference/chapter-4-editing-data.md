---
title: 'Kapitel 4: Bearbeiten von Daten'
TOCTitle: 'Chapter 4: Editing Data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c5364a7b9e70c4627a7f5b4e6708542e2c8516f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474395"
---
# <a name="chapter-4-editing-data"></a>Kapitel 4: Bearbeiten von Daten


**Betrifft**: Access 2013 | Office 2013

In den beiden vorangegangenen Kapiteln wurde erläutert, wie Sie mithilfe von ADO eine Verbindung mit einer Datenquelle herstellen, einen Befehl ausführen, die Ergebnisse in einem **Recordset** -Objekt abrufen sowie innerhalb des **Recordset** -Objekts navigieren. Dieses Kapitel befasst sich mit dem nächsten grundlegenden ADO-Vorgang, nämlich dem Bearbeiten von Daten.

In diesem Kapitel wird weiterhin das **Recordset** -Beispielobjekt aus Kapitel 3 verwendet, jedoch mit einer wichtigen Änderung. Der folgende Code wird zum Öffnen des **Recordset** -Objekts verwendet:

```vb 
 
 . . . 
'BeginEditIntro 
 Dim strSQL As String 
 Dim objRs1 As ADODB.Recordset 
 
 strSQL = "SELECT * FROM Shippers" 
 
 Set objRs1 = New ADODB.Recordset 
 
 objRs1.Open strSQL, GetNewConnection, adOpenStatic, _ 
 adLockBatchOptimistic, adCmdText 
 
 ' Disconnect the Recordset from the Connection object. 
 Set objRs1.ActiveConnection = Nothing 
'EndEditIntro 
 
 
 . . . 
```

Die wichtige Änderung am Code beinhaltet das Festlegen der CursorLocation-Eigenschaft des Connection-Objekts auf adUseClient in der GetNewConnection-Funktion (siehe unten), womit die Verwendung eines Clientcursors definiert wird. Weitere Informationen zu den Unterschieden zwischen client- und serverseitigen Cursorn finden Sie in Kapitel 8: Grundlegendes zu Cursorn und Sperren.

Durch die **adUseClient** -Einstellung der **CursorLocation** -Eigenschaft wird die Cursorposition von der Datenquelle (in diesem Fall der Computer mit SQL Server) zur Position des Clientcodes (die Desktoparbeitsstation) verschoben. Diese Einstellung erzwingt, dass ADO Client Cursor Engine für OLE DB im Client aufruft, um den Cursor zu erstellen und zu verwalten.

Möglicherweise haben Sie bemerkt, dass der **LockType** -Parameter der **Open** -Methode in **adLockBatchOptimistic** geändert wurde. Damit wird der Cursor im Batchmodus geöffnet. (Der Anbieter speichert mehrere Änderungen und schreibt sie nur dann in die zugrunde liegende Datenquelle, wenn Sie die **UpdateBatch** -Methode aufrufen.) Änderungen am **Recordset** -Objekt werden erst in der Datenbank aktualisiert, wenn die **UpdateBatch** -Methode aufgerufen wird.

Schließlich verwendet der Code in diesem Kapitel eine geänderte Version der in Kapitel 2 eingeführten GetNewConnection-Funktion. Diese Version der Funktion gibt jetzt einen clientseitigen Cursor zurück. Diese Funktion sieht folgendermaßen aus:

```vb 
 
'BeginNewConnection 
Public Function GetNewConnection() As ADODB.Connection 
 Dim objConn1 As ADODB.Connection 
 Set objConn1 = New ADODB.Connection 
 
 strConnStr = "Provider=SQLOLEDB;Initial Catalog=Northwind;" & _ 
 "Data Source=MySrvr;Integrated Security=SSPI;" 
 
 objConn1.ConnectionString = strConnStr 
 objConn1.CursorLocation = adUseClient 
 objConn1.Open 
 
 Set GetNewConnection = objConn1 
End Function 
'EndNewConnection 
```

