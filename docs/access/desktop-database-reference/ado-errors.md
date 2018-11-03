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
# <a name="ado-errors"></a><span data-ttu-id="2f16f-102">ADO-Fehler</span><span class="sxs-lookup"><span data-stu-id="2f16f-102">ADO errors</span></span>

<span data-ttu-id="2f16f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f16f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f16f-104">ADO-Fehler werden dem Programm als Laufzeitfehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="2f16f-104">ADO Errors are reported to your program as run-time errors.</span></span> <span data-ttu-id="2f16f-105">Sie können den Fehlerbehandlung Mechanismus für die Programmiersprache abzufangen und zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="2f16f-105">You can use the error-trapping mechanism of your programming language to trap and handle them.</span></span> <span data-ttu-id="2f16f-106">Verwenden Sie in Visual Basic beispielsweise die **On Error** -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="2f16f-106">For example, in Visual Basic, use the **On Error** statement.</span></span> <span data-ttu-id="2f16f-107">Verwenden Sie in Visual J++ einen **Try-Catch** -Block.</span><span class="sxs-lookup"><span data-stu-id="2f16f-107">In Visual J++, use a **try-catch** block.</span></span> <span data-ttu-id="2f16f-108">In Visual C++ hängt von der Methode, die Sie verwenden, um die ADO-Bibliotheken zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2f16f-108">In Visual C++, it depends on the method you are using to access the ADO libraries.</span></span> <span data-ttu-id="2f16f-109">Mit \#importieren, verwenden Sie einen **Try-Catch** -Block.</span><span class="sxs-lookup"><span data-stu-id="2f16f-109">With \#import, use a **try-catch** block.</span></span> <span data-ttu-id="2f16f-110">Andernfalls müssen C++-Programmierer explizit das Error-Objekt abrufen, indem **GetErrorInfo**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2f16f-110">Otherwise, C++ programmers need to explicitly retrieve the error object by calling **GetErrorInfo**.</span></span> <span data-ttu-id="2f16f-111">Das folgende Visual Basic Sub-Prozedur veranschaulicht das Beheben eines ADO-Fehlers:</span><span class="sxs-lookup"><span data-stu-id="2f16f-111">The following Visual Basic sub procedure demonstrates trapping an ADO error:</span></span>

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

<span data-ttu-id="2f16f-112">Dies **Formular\_Load** Ereignisprozedur erstellt absichtlich einen Fehler durch **dasselbe Verbindungsobjekt** zweimal öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="2f16f-112">This **Form\_Load** event procedure intentionally creates an error by trying to open the same **Connection** object twice.</span></span> <span data-ttu-id="2f16f-113">Beim zweiten Aufruf der **Open** -Methode wird der Fehlerhandler aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2f16f-113">The second time the **Open** method is called, the error handler is activated.</span></span> <span data-ttu-id="2f16f-114">In diesem Fall ist der Fehler vom Typ **adErrObjectOpen**, weshalb der Fehlerhandler die folgende Fehlermeldung anzeigt, bevor die Ausführung des Programms fortgesetzt wird:</span><span class="sxs-lookup"><span data-stu-id="2f16f-114">In this case the error is of type **adErrObjectOpen**, so the error handler displays the following message before resuming program execution:</span></span>

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

<span data-ttu-id="2f16f-p103">Die Fehlermeldung enthält alle Informationselemente, die vom **Err** -Objekt von Visual Basic bereitgestellt werden, außer dem Wert **LastDLLError**, der in diesem Fall nicht zutrifft. Die Fehlernummer bezeichnet den aufgetretenen Fehler. Die Beschreibung ist für jene Fälle hilfreich, in denen Sie den Fehler nicht selbst behandeln möchten. Sie können sie einfach an den Benutzer weitergeben. Normalerweise werden Sie zwar für Ihre Anwendung angepasste Fehlermeldungen verwenden, aber nicht jeder Fehler kann im voraus berücksichtigt werden. Die Beschreibung liefert einen Hinweis, was schief gelaufen ist. Im Beispielcode wurde der Fehler vom **Connection** -Objekt gemeldet. In diesem Fall wird kein Variablenname, sondern der Objekttyp oder die Programm-ID angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f16f-p103">The error message includes each piece of information provided by the Visual Basic **Err** object except for the **LastDLLError** value, which does not apply here. The error number tells you which error has occurred. The description is useful in cases in which you do not want to handle the error yourself. You can simply pass it along to the user. Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong. In the sample code, the error was reported by the **Connection** object. You will see the object's type or programmatic ID here — not a variable name.</span></span>


> [!NOTE]
> <span data-ttu-id="2f16f-p104">[!HINWEIS] Das **Err** -Objekt von Visual Basic enthält nur Informationen zum letzten Fehler. Die **Errors** -Auflistung von ADO des **Connection** -Objekts enthält ein **Error** -Objekt pro Fehler, der vom letzten ADO-Vorgang ausgelöst wurde. Verwenden Sie die **Errors** -Auflistung anstelle des **Err** -Objekts, um mehrere Fehler zu behandeln. Weitere Informationen zur **Errors** -Auflistung finden Sie unter <A href="provider-errors.md">Anbieterfehler</A>. Wenn jedoch kein gültiges **Connection** -Objekt vorhanden ist, stellt das **Err** -Objekt die einzige Informationsquelle für ADO-Fehler dar.</span><span class="sxs-lookup"><span data-stu-id="2f16f-p104">The Visual Basic **Err** object only contains information about the most recent error. The ADO **Errors** collection of the **Connection** object contains one **Error** object for each error raised by the most recent ADO operation. Use the **Errors** collection rather than the **Err** object to handle multiple errors. For more information about the **Errors** collection, see <A href="provider-errors.md">Provider Errors</A>. However, if there is no valid **Connection** object, the **Err** object is the only source for information about ADO errors.</span></span>

<span data-ttu-id="2f16f-p105">Durch welche Vorgänge werden wahrscheinlich ADO-Fehler verursacht? Zu häufigen ADO-Fehlern zählt das Öffnen eines Objekts wie z. B. eines **Connection** - oder **Recordset** -Objekts, das Aktualisieren von Daten oder das Aufrufen einer Methode oder Eigenschaft, die von Ihrem Anbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2f16f-p105">What kinds of operations are likely to cause ADO errors? Common ADO errors can involve opening an object such as a **Connection** or **Recordset**, attempting to update data, or calling a method or property that is not supported by your provider.</span></span>

<span data-ttu-id="2f16f-p106">OLE DB-Fehler können außerdem in der **Errors** -Auflistung als Laufzeitfehler an die Anwendung übergeben werden. Weitere Informationen zu OLE DB-Fehlernummern finden Sie in Kapitel 16 der OLE DB-Programmierreferenz.</span><span class="sxs-lookup"><span data-stu-id="2f16f-p106">OLE DB errors can also be passed to your application as run-time errors in the **Errors** collection. For more information about OLE DB error numbers, see Chapter 16 of the OLE DB Programmer's Reference.</span></span>

