---
title: Ereignisparameter (Access PC-Datenbank-Referenz)
TOCTitle: Event Parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 023109586d13dc25846c8c145746aaf97fc22c15
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888370"
---
# <a name="event-parameters"></a><span data-ttu-id="f708d-102">Ereignisparameter</span><span class="sxs-lookup"><span data-stu-id="f708d-102">Event Parameters</span></span>


<span data-ttu-id="f708d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f708d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f708d-p101">Jeder Ereignishandler hat einen Statusparameter, durch den der Ereignishandler gesteuert wird. Für Complete-Ereignisse wird dieser Parameter auch verwendet, um den Erfolg oder das Fehlschlagen der Operation, durch die das Ereignis generiert wurde, anzugeben. Die meisten Complete-Ereignisse haben auch einen Fehlerparameter zum Bereitstellen von Informationen zu möglicherweise aufgetretenen Fehlern sowie mindestens einen Objektparameter, durch den auf die zum Ausführen der Operation verwendeten ADO-Objekte verwiesen wird. Beispielsweise enthält das ExecuteComplete-Ereignis Objektparameter für die dem Ereignis zugeordneten Objekte Command, Recordset und Connection. Im folgenden Beispiel für Microsoft Visual Basic sehen Sie die Objekte pCommand, pRecordset und pConnection, die die von der Execute-Methode verwendeten Objekte Command, Recordset und Connection darstellen.</span><span class="sxs-lookup"><span data-stu-id="f708d-p101">Every event handler has a status parameter that controls the event handler. For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event. Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation. For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event. In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="f708d-p102">Abgesehen vom Error-Objekt werden den Will-Ereignissen die gleichen Parameter übergeben. Dadurch haben Sie Gelegenheit, die einzelnen für die ausstehende Operation zu verwendenden Objekte zu untersuchen und zu ermitteln, ob die Operation abgeschlossen werden darf.</span><span class="sxs-lookup"><span data-stu-id="f708d-p102">Except for the **Error** object, the same parameters are passed to the Will events. This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="f708d-p103">Manche Ereignishandler haben einen *Reason*-Parameter, durch den zusätzliche Informationen zum Grund des Auftretens des Ereignisses bereitgestellt werden. Beispielsweise können die Ereignisse **WillMove** und **MoveComplete** auftreten, weil eine der Navigationsmethoden (**MoveNext**, **MovePrevious** usw.) aufgerufen wird oder weil sie das Ergebnis einer erneuten Abfrage sind.</span><span class="sxs-lookup"><span data-stu-id="f708d-p103">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred. For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="f708d-113">Status-Parameter</span><span class="sxs-lookup"><span data-stu-id="f708d-113">Status Parameter</span></span>

<span data-ttu-id="f708d-114">Wenn die Ereignishandlerroutine aufgerufen wird, wird der *Status*-Parameter auf einen der folgenden Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f708d-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f708d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f708d-115">Value</span></span></p></th>
<th><p><span data-ttu-id="f708d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f708d-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f708d-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="f708d-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="f708d-p104">Wird den Ereignissen Will und Complete übergeben. Dieser Wert bedeutet, dass die Operation, durch die das Ereignis verursacht wurde, erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f708d-p104">Passed to both Will and Complete events. This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f708d-120"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="f708d-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="f708d-p105">Wird nur Complete-Ereignissen übergeben. Dieser Wert bedeutet, dass die Operation, durch die das Ereignis verursacht wurde, nicht erfolgreich war oder von einem Will-Ereignis abgebrochen wurde. Überprüfen Sie den Error-Parameter auf weitere Details.</span><span class="sxs-lookup"><span data-stu-id="f708d-p105">Passed to Complete events only. This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation. Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f708d-124"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="f708d-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="f708d-p106">Wird nur Will-Ereignissen übergeben. Dieser Wert bedeutet, dass die Operation vom Will-Ereignis nicht abgebrochen werden kann. Sie muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f708d-p106">Passed to Will events only. This value means that the operation cannot be canceled by the Will event. It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f708d-p107">Wenn Sie im Will-Ereignis ermitteln, dass die Operation fortgesetzt werden soll, lassen Sie den Status-Parameter unverändert. Solange der eingehende Statusparameter nicht auf adStatusCantDeny festgelegt wurde, können Sie die ausstehende Operation abbrechen, indem Sie Status in adStatusCancel ändern. Wenn Sie dies tun, wird der Status-Parameter des der Operation zugeordneten Complete-Ereignisses auf adStatusErrorsOccurred festgelegt. Das dem Complete-Ereignis übergebene Error-Objekt enthält den Wert adErrOperationCancelled.</span><span class="sxs-lookup"><span data-stu-id="f708d-p107">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged. As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**. When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**. The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="f708d-p108">Wenn ein Ereignis nicht mehr verarbeitet werden soll, können Sie *Status* auf **adStatusUnwantedEvent** festlegen, und die Anwendung empfängt keine Benachrichtigungen mehr für dieses Ereignis. Manche Ereignisse können jedoch aus mehreren Gründen ausgelöst werden. In diesem Fall müssen Sie **adStatusUnwantedEvent** für jeden möglichen Grund angeben. Zum Beenden des Empfangs von Benachrichtigungen zu ausstehenden **RecordChange**-Ereignissen z. B. müssen Sie den *Status*-Parameter für die auftretenden Ereignisse **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** und **adRsnFirstChange** auf **adStatusUnwantedEvent** festlegen.</span><span class="sxs-lookup"><span data-stu-id="f708d-p108">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event. Remember, however, that some events can be raised for more than one reason. In that case, you must specify **adStatusUnwantedEvent** for each possible reason. For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f708d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="f708d-136">Value</span></span></p></th>
<th><p><span data-ttu-id="f708d-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f708d-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f708d-138"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="f708d-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="f708d-139">Es wird angefordert, dass dieser Ereignishandler keine weiteren Benachrichtigungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="f708d-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f708d-140"><strong>adStatusCancel fest</strong></span><span class="sxs-lookup"><span data-stu-id="f708d-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="f708d-141">Es wird angefordert, dass die Operation, die gerade auftreten soll, abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="f708d-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="f708d-142">Error-Parameter</span><span class="sxs-lookup"><span data-stu-id="f708d-142">Error Parameter</span></span>

<span data-ttu-id="f708d-p109">Der Error-Parameter ist ein Verweis auf ein Error-ADO-Objekt. Wenn der Status-Parameter auf adStatusErrorsOccurred festgelegt ist, enthält das Error-Objekt Details zum Grund für das Fehlschlagen der Operation. Wenn die Operation von dem einem Complete-Ereignis zugeordneten Will-Ereignis durch Festlegen des Status-Parameters auf adStatusCancel abgebrochen wurde, wird das Fehlerobjekt immer auf adErrOperationCancelled festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f708d-p109">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object. When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed. If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="f708d-146">Object-Parameter</span><span class="sxs-lookup"><span data-stu-id="f708d-146">Object Parameter</span></span>

<span data-ttu-id="f708d-p110">Jedes Ereignis empfängt eines oder mehrere Objekte, die die Objekte darstellen, die an der Operation beteiligt sind. Beispielsweise empfängt das **ExecuteComplete** -Ereignis ein **Command** -Objekt, ein **Recordset** -Objekt und ein **Connection** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f708d-p110">Each event receives one or more objects representing the objects that are involved in the operation. For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="f708d-149">Reason-Parameter</span><span class="sxs-lookup"><span data-stu-id="f708d-149">Reason Parameter</span></span>

<span data-ttu-id="f708d-p111">Durch den Reason-Parameter adReason werden zusätzliche Informationen zum Grund des Auftretens des Ereignisses bereitgestellt. Ereignisse mit einem adReason-Parameter können selbst für die gleiche Operation jeweils aus unterschiedlichen Gründen mehrmals aufgerufen werden. Beispielsweise wird der WillChangeRecord-Ereignishandler aufgerufen für Operationen, bei denen die Einfügung, Löschung oder Änderung eines Datensatzes ausgeführt oder rückgängig gemacht werden soll. Wenn ein Ereignis nur bei Auftreten aus einem bestimmten Grund verarbeitet werden soll, können Sie mithilfe des adReason-Parameters die aufgetretenen Ereignisse, an denen Sie nicht interessiert sind, herausfiltern. Beispielsweise können Sie, wenn record-change-Ereignisse nur bei Auftreten aufgrund der Hinzufügung eines Datensatzes verarbeitet werden sollen, folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="f708d-p111">The *Reason* parameter, *adReason*, provides additional information about why the event occurred. Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason. For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record. If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in. For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

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

<span data-ttu-id="f708d-p112">In diesem Fall kann die Benachrichtigung potenziell aus jedem der anderen Gründe auftreten. Sie tritt jedoch nur ein Mal für jeden Grund auf. Wenn die Benachrichtigung für jeden Grund ein Mal aufgetreten ist, empfangen Sie nur Benachrichtigungen für die Hinzufügung eines neuen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="f708d-p112">In this case, notification can potentially occur for each of the other reasons. However, it will occur only once for each reason. After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="f708d-158">Im Gegensatz dazu müssen Sie *AdStatus* auf **adStatusUnwantedEvent fest,** nur einmal festlegen anfordern, die einen Ereignishandler ohne eine **AdReason** -Parameter keine Benachrichtigungen mehr empfängt.</span><span class="sxs-lookup"><span data-stu-id="f708d-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

