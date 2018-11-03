---
title: 'Kapitel 4: Bearbeiten von Daten'
TOCTitle: 'Chapter 4: Editing data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28103cebeea517395ce2507402677fcde8114bb0
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936588"
---
# <a name="chapter-4-editing-data"></a><span data-ttu-id="a7afc-102">Kapitel 4: Bearbeiten von Daten</span><span class="sxs-lookup"><span data-stu-id="a7afc-102">Chapter 4: Editing data</span></span>

<span data-ttu-id="a7afc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7afc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7afc-p101">In den beiden vorangegangenen Kapiteln wurde erläutert, wie Sie mithilfe von ADO eine Verbindung mit einer Datenquelle herstellen, einen Befehl ausführen, die Ergebnisse in einem **Recordset** -Objekt abrufen sowie innerhalb des **Recordset** -Objekts navigieren. Dieses Kapitel befasst sich mit dem nächsten grundlegenden ADO-Vorgang, nämlich dem Bearbeiten von Daten.</span><span class="sxs-lookup"><span data-stu-id="a7afc-p101">The preceding two chapters explained how use ADO to connect to a data source, execute a command, get the results in a **Recordset** object, and navigate within the **Recordset**. This chapter focuses on the next fundamental ADO operation: editing data.</span></span>

<span data-ttu-id="a7afc-p102">In diesem Kapitel wird weiterhin das **Recordset** -Beispielobjekt aus Kapitel 3 verwendet, jedoch mit einer wichtigen Änderung. Der folgende Code wird zum Öffnen des **Recordset** -Objekts verwendet:</span><span class="sxs-lookup"><span data-stu-id="a7afc-p102">This chapter continues to use the sample **Recordset** introduced in Chapter 3 — with one important change. The following code is used to open the **Recordset**:</span></span>

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

<span data-ttu-id="a7afc-p103">Die wichtige Änderung am Code beinhaltet das Festlegen der CursorLocation-Eigenschaft des Connection-Objekts auf adUseClient in der GetNewConnection-Funktion (siehe unten), womit die Verwendung eines Clientcursors definiert wird. Weitere Informationen zu den Unterschieden zwischen client- und serverseitigen Cursorn finden Sie in Kapitel 8: Grundlegendes zu Cursorn und Sperren.</span><span class="sxs-lookup"><span data-stu-id="a7afc-p103">The important change to the code involves setting the **Connection** object's **CursorLocation** property equal to **adUseClient** in the GetNewConnection function (shown below), which indicates the use of a client cursor. For more information about the differences between client-side and server-side cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

<span data-ttu-id="a7afc-p104">Durch die **adUseClient** -Einstellung der **CursorLocation** -Eigenschaft wird die Cursorposition von der Datenquelle (in diesem Fall der Computer mit SQL Server) zur Position des Clientcodes (die Desktoparbeitsstation) verschoben. Diese Einstellung erzwingt, dass ADO Client Cursor Engine für OLE DB im Client aufruft, um den Cursor zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a7afc-p104">The **CursorLocation** property's **adUseClient** setting moves the location of the cursor from the data source (the SQL Server, in this case) to the location of the client code (the desktop workstation). This setting forces ADO to invoke the Client Cursor Engine for OLE DB on the client in order to create and manage the cursor.</span></span>

<span data-ttu-id="a7afc-p105">Möglicherweise haben Sie bemerkt, dass der **LockType** -Parameter der **Open** -Methode in **adLockBatchOptimistic** geändert wurde. Damit wird der Cursor im Batchmodus geöffnet. (Der Anbieter speichert mehrere Änderungen und schreibt sie nur dann in die zugrunde liegende Datenquelle, wenn Sie die **UpdateBatch** -Methode aufrufen.) Änderungen am **Recordset** -Objekt werden erst in der Datenbank aktualisiert, wenn die **UpdateBatch** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a7afc-p105">You might also have noticed that the **LockType** parameter of the **Open** method changed to **adLockBatchOptimistic**. This opens the cursor in batch mode. (The provider caches multiple changes and writes them to the underlying data source only when you call the **UpdateBatch** method.) Changes made to the **Recordset** will not be updated in the database until the **UpdateBatch** method is called.</span></span>

<span data-ttu-id="a7afc-p106">Schließlich verwendet der Code in diesem Kapitel eine geänderte Version der in Kapitel 2 eingeführten GetNewConnection-Funktion. Diese Version der Funktion gibt jetzt einen clientseitigen Cursor zurück. Diese Funktion sieht folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="a7afc-p106">Finally, the code in this chapter uses a modified version of the GetNewConnection function, introduced in Chapter 2. This version of the function now returns a client-side cursor. The function looks like this:</span></span>

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

<span data-ttu-id="a7afc-118">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="a7afc-118">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="a7afc-119">Bearbeiten vorhandener Datensätze</span><span class="sxs-lookup"><span data-stu-id="a7afc-119">Editing existing records</span></span>](editing-existing-records.md)
- [<span data-ttu-id="a7afc-120">Bestimmen der unterstützten Funktionalität</span><span class="sxs-lookup"><span data-stu-id="a7afc-120">Determining what is supported</span></span>](determining-what-is-supported.md)
- [<span data-ttu-id="a7afc-121">Löschen von Datensätzen mithilfe der Delete-Methode</span><span class="sxs-lookup"><span data-stu-id="a7afc-121">Deleting records using the Delete method</span></span>](deleting-records-using-the-delete-method.md)
- [<span data-ttu-id="a7afc-122">Alternativen: Verwenden von SQL-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="a7afc-122">Alternatives: using SQL statements</span></span>](alternatives-using-sql-statements.md)
- [<span data-ttu-id="a7afc-123">Hinzufügen von Datensätzen (ADO)</span><span class="sxs-lookup"><span data-stu-id="a7afc-123">Adding records (ADO)</span></span>](adding-records.md)