---
title: Ereignisparameter (Access PC-Datenbank-Referenz)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dd4a99ec24a05084a2ae137ded3219c2997f8cf3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720492"
---
# <a name="event-parameters"></a>Ereignisparameter

**Betrifft**: Access 2013, Office 2013

Jeder Ereignishandler hat einen Statusparameter, durch den der Ereignishandler gesteuert wird. Für Complete-Ereignisse wird dieser Parameter auch verwendet, um den Erfolg oder das Fehlschlagen der Operation, durch die das Ereignis generiert wurde, anzugeben. Die meisten Complete-Ereignisse haben auch einen Fehlerparameter zum Bereitstellen von Informationen zu möglicherweise aufgetretenen Fehlern sowie mindestens einen Objektparameter, durch den auf die zum Ausführen der Operation verwendeten ADO-Objekte verwiesen wird. Beispielsweise enthält das ExecuteComplete-Ereignis Objektparameter für die dem Ereignis zugeordneten Objekte Command, Recordset und Connection. Im folgenden Beispiel für Microsoft Visual Basic sehen Sie die Objekte pCommand, pRecordset und pConnection, die die von der Execute-Methode verwendeten Objekte Command, Recordset und Connection darstellen.

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

Abgesehen vom Error-Objekt werden den Will-Ereignissen die gleichen Parameter übergeben. Dadurch haben Sie Gelegenheit, die einzelnen für die ausstehende Operation zu verwendenden Objekte zu untersuchen und zu ermitteln, ob die Operation abgeschlossen werden darf.

Manche Ereignishandler haben einen *Reason*-Parameter, durch den zusätzliche Informationen zum Grund des Auftretens des Ereignisses bereitgestellt werden. Beispielsweise können die Ereignisse **WillMove** und **MoveComplete** auftreten, weil eine der Navigationsmethoden (**MoveNext**, **MovePrevious** usw.) aufgerufen wird oder weil sie das Ergebnis einer erneuten Abfrage sind.

## <a name="status-parameter"></a>Status-Parameter

Wenn die Ereignishandlerroutine aufgerufen wird, wird der *Status*-Parameter auf einen der folgenden Werte festgelegt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>Wird den Ereignissen Will und Complete übergeben. Dieser Wert bedeutet, dass die Operation, durch die das Ereignis verursacht wurde, erfolgreich abgeschlossen wurde.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>Wird nur Complete-Ereignissen übergeben. Dieser Wert bedeutet, dass die Operation, durch die das Ereignis verursacht wurde, nicht erfolgreich war oder von einem Will-Ereignis abgebrochen wurde. Überprüfen Sie den Error-Parameter auf weitere Details.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Wird nur Will-Ereignissen übergeben. Dieser Wert bedeutet, dass die Operation vom Will-Ereignis nicht abgebrochen werden kann. Sie muss ausgeführt werden.</p></td>
</tr>
</tbody>
</table>


Wenn Sie im Will-Ereignis ermitteln, dass die Operation fortgesetzt werden soll, lassen Sie den Status-Parameter unverändert. Solange der eingehende Statusparameter nicht auf adStatusCantDeny festgelegt wurde, können Sie die ausstehende Operation abbrechen, indem Sie Status in adStatusCancel ändern. Wenn Sie dies tun, wird der Status-Parameter des der Operation zugeordneten Complete-Ereignisses auf adStatusErrorsOccurred festgelegt. Das dem Complete-Ereignis übergebene Error-Objekt enthält den Wert adErrOperationCancelled.

Wenn ein Ereignis nicht mehr verarbeitet werden soll, können Sie *Status* auf **adStatusUnwantedEvent** festlegen, und die Anwendung empfängt keine Benachrichtigungen mehr für dieses Ereignis. Manche Ereignisse können jedoch aus mehreren Gründen ausgelöst werden. In diesem Fall müssen Sie **adStatusUnwantedEvent** für jeden möglichen Grund angeben. Zum Beenden des Empfangs von Benachrichtigungen zu ausstehenden **RecordChange**-Ereignissen z. B. müssen Sie den *Status*-Parameter für die auftretenden Ereignisse **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** und **adRsnFirstChange** auf **adStatusUnwantedEvent** festlegen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>Es wird angefordert, dass dieser Ereignishandler keine weiteren Benachrichtigungen empfängt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCancel fest</strong></p></td>
<td><p>Es wird angefordert, dass die Operation, die gerade auftreten soll, abgebrochen wird.</p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a>Error-Parameter

Der Error-Parameter ist ein Verweis auf ein Error-ADO-Objekt. Wenn der Status-Parameter auf adStatusErrorsOccurred festgelegt ist, enthält das Error-Objekt Details zum Grund für das Fehlschlagen der Operation. Wenn die Operation von dem einem Complete-Ereignis zugeordneten Will-Ereignis durch Festlegen des Status-Parameters auf adStatusCancel abgebrochen wurde, wird das Fehlerobjekt immer auf adErrOperationCancelled festgelegt.

## <a name="object-parameter"></a>Object-Parameter

Jedes Ereignis empfängt eines oder mehrere Objekte, die die Objekte darstellen, die an der Operation beteiligt sind. Beispielsweise empfängt das **ExecuteComplete** -Ereignis ein **Command** -Objekt, ein **Recordset** -Objekt und ein **Connection** -Objekt.

## <a name="reason-parameter"></a>Reason-Parameter

Durch den Reason-Parameter adReason werden zusätzliche Informationen zum Grund des Auftretens des Ereignisses bereitgestellt. Ereignisse mit einem adReason-Parameter können selbst für die gleiche Operation jeweils aus unterschiedlichen Gründen mehrmals aufgerufen werden. Beispielsweise wird der WillChangeRecord-Ereignishandler aufgerufen für Operationen, bei denen die Einfügung, Löschung oder Änderung eines Datensatzes ausgeführt oder rückgängig gemacht werden soll. Wenn ein Ereignis nur bei Auftreten aus einem bestimmten Grund verarbeitet werden soll, können Sie mithilfe des adReason-Parameters die aufgetretenen Ereignisse, an denen Sie nicht interessiert sind, herausfiltern. Beispielsweise können Sie, wenn record-change-Ereignisse nur bei Auftreten aufgrund der Hinzufügung eines Datensatzes verarbeitet werden sollen, folgende Aktionen ausführen:

```vb 
 
' BeginEventExampleVB01 
Private Sub rsTest_WillChangeRecord(ByVal adReason As ADODB.EventReasonEnum, ByVal cRecords As Long, adStatus As ADODB.EventStatusEnum, ByVal pRecordset As ADODB.Recordset) 
 If adReason = adRsnAddNew Then 
 ' Process event 
 '... 
 Else 
 ' Cancel event notification for all 
 ' other possible adReason values. 
 adStatus = adStatusUnwantedEvent 
 End If 
End Sub 
' EndEventExampleVB01 
```

In diesem Fall kann die Benachrichtigung potenziell aus jedem der anderen Gründe auftreten. Sie tritt jedoch nur ein Mal für jeden Grund auf. Wenn die Benachrichtigung für jeden Grund ein Mal aufgetreten ist, empfangen Sie nur Benachrichtigungen für die Hinzufügung eines neuen Datensatzes.

Im Gegensatz dazu müssen Sie *AdStatus* auf **adStatusUnwantedEvent fest,** nur einmal festlegen anfordern, die einen Ereignishandler ohne eine **AdReason** -Parameter keine Benachrichtigungen mehr empfängt.

