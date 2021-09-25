---
title: Visual Basic (Access-Desktopdatenbankreferenz)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fe56644d4bfe307ac3b9e42af94e7566b2507c9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593264"
---
# <a name="visual-basic"></a>Visual Basic


**Gilt für**: Access 2013, Office 2013

Um ADO-Ereignisse in Microsoft Visual Basic zu behandeln, müssen Sie mithilfe des **WithEvents** -Schlüsselworts eine Variable auf Modulebene deklarieren. Die Variable kann nur als Teil eines Klassenmoduls deklariert werden und muss auf der Modulebene deklariert werden. Dies ist jedoch weniger restriktiv als es den Anschein hat, weil **Form** -Objekte von Visual Basic ebenfalls Klassen sind. Die einfachste Methode zum Behandeln von ADO-Ereignissen ist das Deklarieren einer Variablen mithilfe von **WithEvents**. Im folgenden Beispiel wird das **ConnectComplete** -Ereignis für ein **Connection** -Objekt behandelt:

```vb 
 
' BeginEventExampleVB02 
Dim WithEvents connEvent As Connection 
Attribute connEvent.VB_VarHelpID = -1 
Dim strMsg As String 
 
Private Sub Form_Load() 
 On Error GoTo ErrHandler: 
 
 Dim strConn As String 
 
 ' Create a new object with event 
 ' handling enabled. 
 strConn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';" & _ 
 "Integrated Security='SSPI';" 
 Set connEvent = New ADODB.Connection 
 connEvent.Open strConn 
 
 Exit Sub 
 
ErrHandler: 
 MsgBox strMsg 
End Sub 
 
Private Sub connEvent_ConnectComplete(ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pConnection As ADODB.Connection) 
 
 If adStatus = adStatusErrorsOccurred Then 
 If Not pError Is Nothing Then 
 Select Case pError.Number 
 Case adErrOperationCancelled 
 ' The operation was cancelled in the 
 ' Will event. Notify the user and exit. 
 strMsg = "I'm sorry you can't connect right now." & vbCrLf 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 Case Else 
 strMsg = "Error " & Format(pError.Number) & vbCrLf 
 strMsg = strMsg & pError.Description 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 End Select 
 Else 
 strMsg = "Error occured. Click OK to exit." 
 Unload Me 
 End If 
 End If 
 'frmWait.btnOK.Enabled = True 
End Sub 
' EndEventExampleVB02 
```

The **Connection** object is declared at the **Form** level using the **WithEvents** keyword to enable event handling. Der Form \_ Load-Ereignishandler erstellt tatsächlich das Objekt, indem er *connEvent* ein neues **Connection-Objekt** zuweist und dann die Verbindung öffnet. Natürlich würde eine echte Anwendung mehr Verarbeitung im Form \_ Load-Ereignishandler ausführen, als hier gezeigt wird.

