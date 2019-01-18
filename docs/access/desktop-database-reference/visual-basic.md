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
# <a name="visual-basic"></a><span data-ttu-id="e6e10-102">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e6e10-102">Visual Basic</span></span>


<span data-ttu-id="e6e10-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6e10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6e10-p101">Um ADO-Ereignisse in Microsoft Visual Basic zu behandeln, müssen Sie mithilfe des **WithEvents** -Schlüsselworts eine Variable auf Modulebene deklarieren. Die Variable kann nur als Teil eines Klassenmoduls deklariert werden und muss auf der Modulebene deklariert werden. Dies ist jedoch weniger restriktiv als es den Anschein hat, weil **Form** -Objekte von Visual Basic ebenfalls Klassen sind. Die einfachste Methode zum Behandeln von ADO-Ereignissen ist das Deklarieren einer Variablen mithilfe von **WithEvents**. Im folgenden Beispiel wird das **ConnectComplete** -Ereignis für ein **Connection** -Objekt behandelt:</span><span class="sxs-lookup"><span data-stu-id="e6e10-p101">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword. The variable can be declared only as part of a class module and must be declared at the module level. This is not as restrictive as it seems, however, because Visual Basic **Form** objects are also classes. The simplest way to handle ADO events is to declare a variable using **WithEvents**. The following example handles the **ConnectComplete** event for a **Connection** object:</span></span>

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

<span data-ttu-id="e6e10-109">Das **Connection** -Objekt wird auf **Formularebene verwenden das Schlüsselwort **WithEvents** zum ermöglichen des Ereignisbehandlung** deklariert.</span><span class="sxs-lookup"><span data-stu-id="e6e10-109">The **Connection** object is declared at the **Form** level using the **WithEvents** keyword to enable event handling.</span></span> <span data-ttu-id="e6e10-110">Das Formular\_Load-Ereignishandler erstellt das Objekt, indem Sie **ein neues Verbindungsobjekt** *ConnEvent* zuweisen, und klicken Sie dann die Verbindung wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e6e10-110">The Form\_Load event handler actually creates the object by assigning a new **Connection** object to *connEvent* and then opens the connection.</span></span> <span data-ttu-id="e6e10-111">Natürlich eine echte Anwendung würden führen Sie weitere Verarbeitung in der Form\_Load-Ereignishandler als hier dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e6e10-111">Of course, a real application would do more processing in the Form\_Load event handler than is shown here.</span></span>

