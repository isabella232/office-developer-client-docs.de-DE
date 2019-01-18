---
title: Visual Basic (Access PC-Datenbank-Referenz)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3045cf3861409d2909f31536670a27c282eb2cdc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709803"
---
# <a name="visual-basic"></a>Visual Basic


**Betrifft**: Access 2013, Office 2013

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

Das **Connection** -Objekt wird auf **Formularebene verwenden das Schlüsselwort **WithEvents** zum ermöglichen des Ereignisbehandlung** deklariert. Das Formular\_Load-Ereignishandler erstellt das Objekt, indem Sie **ein neues Verbindungsobjekt** *ConnEvent* zuweisen, und klicken Sie dann die Verbindung wird geöffnet. Natürlich eine echte Anwendung würden führen Sie weitere Verarbeitung in der Form\_Load-Ereignishandler als hier dargestellt wird.

