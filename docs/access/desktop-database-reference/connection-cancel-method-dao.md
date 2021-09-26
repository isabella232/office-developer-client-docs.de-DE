---
title: Connection.Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: 43ad7b64-823d-3fac-e4d4-5e9514f60011
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192953(v=office.15)
ms:contentKeyID: 48544509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 489f1d1b85fdd9a3ba207f733123cf18af6c91d5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597611"
---
# <a name="connectioncancel-method-dao"></a>Connection.Cancel-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . Abbrechen

*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen **Execute-** oder **OpenConnection-Methodenaufrufs** zu beenden (das heißt, die Methode wurde mit der Option dbRunAsync aufgerufen). **Cancel** gibt einen Laufzeitfehler zurück, wenn dbRunAsync nicht in der Methode verwendet wurde, die Sie beenden möchten.

Wenn Sie nach einem **Cancel**-Methodenaufruf versuchen, auf das Objekt zu verweisen, das durch einen asynchronen **OpenConnection**-Aufruf erstellt worden wäre (also das **Connection**-Objekt, über das Sie die **Cancel**-Methode aufgerufen haben), tritt ein Fehler auf.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die **StillExecuting**-Eigenschaft und die **Cancel**-Methode verwendet, um ein **Connection**-Objekt asynchron zu öffnen.

```vb
    Sub CancelConnectionX() 
     
     Dim wrkMain As Workspace 
     Dim conMain As Connection 
     Dim sngTime As Single 
     
     Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
     "admin", "", dbUseODBC) 
     ' Open the connection asynchronously. 
     
     ' Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conMain = wrkMain.OpenConnection("Publishers", _ 
     dbDriverNoPrompt + dbRunAsync, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     sngTime = Timer 
     
     ' Wait five seconds. 
     Do While Timer - sngTime < 5 
     Loop 
     
     ' If the connection has not been made, ask the user 
     ' if she wants to keep waiting. If she does not, cancel 
     ' the connection and exit the procedure. 
     Do While conMain.StillExecuting 
     
     If MsgBox("No connection yet--keep waiting?", _ 
     vbYesNo) = vbNo Then 
     conMain.Cancel 
     MsgBox "Connection cancelled!" 
     wrkMain.Close 
     Exit Sub 
     End If 
     
     Loop 
     
     With conMain 
     ' Use the Connection object conMain. 
     .Close 
     End With 
     
     wrkMain.Close 
     
    End Sub
```
