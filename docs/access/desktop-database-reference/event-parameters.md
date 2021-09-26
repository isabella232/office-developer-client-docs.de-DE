---
title: Ereignisparameter (Access-Desktopdatenbankreferenz)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 55b5a3cf20e13bc46568c20a375caf442b8c836b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597415"
---
# <a name="event-parameters"></a>Ereignisparameter

**Gilt für**: Access 2013, Office 2013

Every event handler has a status parameter that controls the event handler. For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event. Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation. For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event. In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

Except for the **Error** object, the same parameters are passed to the Will events. This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.

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
<td><p>Wird nur an Complete-Ereignisse übergeben. Dieser Wert bedeutet, dass der Vorgang, der das Ereignis verursacht hat, nicht erfolgreich war, oder dass der Vorgang durch ein Will-Ereignis abgebrochen wurde. Überprüfen Sie den <em>Parameter "Error",</em> um weitere Details zu erhalten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Wird nur Will-Ereignissen übergeben. Dieser Wert bedeutet, dass die Operation vom Will-Ereignis nicht abgebrochen werden kann. Sie muss ausgeführt werden.</p></td>
</tr>
</tbody>
</table>


Wenn Sie im Will-Ereignis festlegen, dass der Vorgang fortgesetzt werden soll, lassen Sie den *Status-Parameter* unverändert. Solange der Parameter für den eingehenden Status nicht auf **"adStatusCantDeny"** festgelegt wurde, können Sie den ausstehenden Vorgang jedoch abbrechen, indem Sie *"Status"* in **"adStatusCancel"** ändern. Wenn Sie dies tun, wird für das dem Vorgang zugeordnete Complete-Ereignis der *Status-Parameter* auf **"adStatusErrorsOccurred"** festgelegt. The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.

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
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>Es wird angefordert, dass die Operation, die gerade auftreten soll, abgebrochen wird.</p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a>Error-Parameter

Der *Error-Parameter* ist ein Verweis auf ein ADO [Error-Objekt.](error-object-ado.md) Wenn der *Status-Parameter* auf **"adStatusErrorsOccurred"** festgelegt ist, enthält das **Error -Objekt** Details dazu, warum der Vorgang fehlgeschlagen ist. Wenn das einem Complete-Ereignis zugeordnete Will-Ereignis den Vorgang abgebrochen hat, indem der *Status-Parameter* auf **"adStatusCancel"** festgelegt wurde, wird das Fehlerobjekt immer auf **"adErrOperationCancelled"** festgelegt.

## <a name="object-parameter"></a>Object-Parameter

Jedes Ereignis empfängt eines oder mehrere Objekte, die die Objekte darstellen, die an der Operation beteiligt sind. Beispielsweise empfängt das **ExecuteComplete**-Ereignis ein **Command**-Objekt, ein **Recordset**-Objekt und ein **Connection**-Objekt.

## <a name="reason-parameter"></a>Reason-Parameter

Der *Parameter Reason,* *adReason,* enthält zusätzliche Informationen dazu, warum das Ereignis aufgetreten ist. Ereignisse mit einem *adReason-Parameter* können mehrmals aufgerufen werden, auch für denselben Vorgang, jedes Mal aus einem anderen Grund. Beispielsweise wird der **WillChangeRecord-Ereignishandler** für Vorgänge aufgerufen, die das Einfügen, Löschen oder Ändern eines Datensatzes ausführen oder rückgängig machen möchten. Wenn Sie ein Ereignis nur verarbeiten möchten, wenn es aus einem bestimmten Grund auftritt, können Sie den *adReason-Parameter* verwenden, um die Vorkommen herauszufiltern, an denen Sie nicht interessiert sind. Wenn Sie beispielsweise Datensatzänderungsereignisse nur verarbeiten möchten, wenn sie auftreten, weil ein Datensatz hinzugefügt wurde, können Sie folgendermaßen vorgehen:

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

Dagegen müssen Sie *adStatus* nur ein Mal auf **adStatusUnwantedEvent** festlegen, um anzufordern, dass ein Ereignishandler ohne **adReason**-Parameter keine Benachrichtigungen mehr empfängt.

