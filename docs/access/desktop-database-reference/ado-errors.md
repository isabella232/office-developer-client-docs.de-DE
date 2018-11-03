---
title: Fehler ActiveX Data Objects (ADO)
TOCTitle: ADO errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e06c0fd79c59e12fe8f7fa3beac65bba37123d56
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944172"
---
# <a name="ado-errors"></a>ADO-Fehler

**Betrifft**: Access 2013, Office 2013

ADO-Fehler werden dem Programm als Laufzeitfehler gemeldet. Sie können den Fehlerbehandlung Mechanismus für die Programmiersprache abzufangen und zu behandeln. Verwenden Sie in Visual Basic beispielsweise die **On Error** -Anweisung. Verwenden Sie in Visual J++ einen **Try-Catch** -Block. In Visual C++ hängt von der Methode, die Sie verwenden, um die ADO-Bibliotheken zugreifen. Mit \#importieren, verwenden Sie einen **Try-Catch** -Block. Andernfalls müssen C++-Programmierer explizit das Error-Objekt abrufen, indem **GetErrorInfo**aufrufen. Das folgende Visual Basic Sub-Prozedur veranschaulicht das Beheben eines ADO-Fehlers:

```vb 
 
' BeginErrorHandlingVB01 
Private Sub Form_Load() 
 ' Turn on error handling 
 On Error GoTo FormLoadError 
 
 'Open the database and the recordset for processing. 
 ' 
 Dim strCnn As String 
 strCnn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 
 ' cnn is a Public Connection Object because 
 ' it was defined WithEvents 
 Set cnn = New ADODB.Connection 
 cnn.Open strCnn 
 
 ' The next line of code intentionally causes 
 ' an error by trying to open a connection 
 ' that has already been opened. 
 cnn.Open strCnn 
 
 ' rst is a Public Recordset because it 
 ' was defined WithEvents 
 Set rst = New ADODB.Recordset 
 rst.Open "Customers", cnn 
 
 Exit Sub 
 
' Error handler 
FormLoadError: 
 Dim strErr As String 
 Select Case Err 
 Case adErrObjectOpen 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 strErr = strErr & "Error reported by: " & Err.Source & vbCrLf 
 strErr = strErr & "Help File: " & Err.HelpFile & vbCrLf 
 strErr = strErr & "Topic ID: " & Err.HelpContext 
 MsgBox strErr 
 Debug.Print strErr 
 Err.Clear 
 Resume Next 
 ' If some other error occurs that 
 ' has nothing to do with ADO, show 
 ' the number and description and exit. 
 Case Else 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 MsgBox strErr 
 Debug.Print strErr 
 Unload Me 
 End Select 
End Sub 
' EndErrorHandlingVB01 
```

Dies **Formular\_Load** Ereignisprozedur erstellt absichtlich einen Fehler durch **dasselbe Verbindungsobjekt** zweimal öffnen möchten. Beim zweiten Aufruf der **Open** -Methode wird der Fehlerhandler aktiviert. In diesem Fall ist der Fehler vom Typ **adErrObjectOpen**, weshalb der Fehlerhandler die folgende Fehlermeldung anzeigt, bevor die Ausführung des Programms fortgesetzt wird:

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

Die Fehlermeldung enthält alle Informationselemente, die vom **Err** -Objekt von Visual Basic bereitgestellt werden, außer dem Wert **LastDLLError**, der in diesem Fall nicht zutrifft. Die Fehlernummer bezeichnet den aufgetretenen Fehler. Die Beschreibung ist für jene Fälle hilfreich, in denen Sie den Fehler nicht selbst behandeln möchten. Sie können sie einfach an den Benutzer weitergeben. Normalerweise werden Sie zwar für Ihre Anwendung angepasste Fehlermeldungen verwenden, aber nicht jeder Fehler kann im voraus berücksichtigt werden. Die Beschreibung liefert einen Hinweis, was schief gelaufen ist. Im Beispielcode wurde der Fehler vom **Connection** -Objekt gemeldet. In diesem Fall wird kein Variablenname, sondern der Objekttyp oder die Programm-ID angezeigt.


> [!NOTE]
> [!HINWEIS] Das **Err** -Objekt von Visual Basic enthält nur Informationen zum letzten Fehler. Die **Errors** -Auflistung von ADO des **Connection** -Objekts enthält ein **Error** -Objekt pro Fehler, der vom letzten ADO-Vorgang ausgelöst wurde. Verwenden Sie die **Errors** -Auflistung anstelle des **Err** -Objekts, um mehrere Fehler zu behandeln. Weitere Informationen zur **Errors** -Auflistung finden Sie unter <A href="provider-errors.md">Anbieterfehler</A>. Wenn jedoch kein gültiges **Connection** -Objekt vorhanden ist, stellt das **Err** -Objekt die einzige Informationsquelle für ADO-Fehler dar.

Durch welche Vorgänge werden wahrscheinlich ADO-Fehler verursacht? Zu häufigen ADO-Fehlern zählt das Öffnen eines Objekts wie z. B. eines **Connection** - oder **Recordset** -Objekts, das Aktualisieren von Daten oder das Aufrufen einer Methode oder Eigenschaft, die von Ihrem Anbieter nicht unterstützt wird.

OLE DB-Fehler können außerdem in der **Errors** -Auflistung als Laufzeitfehler an die Anwendung übergeben werden. Weitere Informationen zu OLE DB-Fehlernummern finden Sie in Kapitel 16 der OLE DB-Programmierreferenz.

