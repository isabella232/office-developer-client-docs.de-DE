---
title: Ereignisparameter (Access-Desktop-Daten Bankreferenz)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dd4a99ec24a05084a2ae137ded3219c2997f8cf3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293315"
---
# <a name="event-parameters"></a><span data-ttu-id="d20b3-102">Ereignisparameter</span><span class="sxs-lookup"><span data-stu-id="d20b3-102">Event parameters</span></span>

<span data-ttu-id="d20b3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d20b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d20b3-p101">Every event handler has a status parameter that controls the event handler. For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event. Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation. For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event. In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span><span class="sxs-lookup"><span data-stu-id="d20b3-p101">Every event handler has a status parameter that controls the event handler. For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event. Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation. For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event. In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="d20b3-p102">Except for the **Error** object, the same parameters are passed to the Will events. This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span><span class="sxs-lookup"><span data-stu-id="d20b3-p102">Except for the **Error** object, the same parameters are passed to the Will events. This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="d20b3-p103">Manche Ereignishandler haben einen *Reason*-Parameter, durch den zusätzliche Informationen zum Grund des Auftretens des Ereignisses bereitgestellt werden. Beispielsweise können die Ereignisse **WillMove** und **MoveComplete** auftreten, weil eine der Navigationsmethoden (**MoveNext**, **MovePrevious** usw.) aufgerufen wird oder weil sie das Ergebnis einer erneuten Abfrage sind.</span><span class="sxs-lookup"><span data-stu-id="d20b3-p103">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred. For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="d20b3-113">Status-Parameter</span><span class="sxs-lookup"><span data-stu-id="d20b3-113">Status Parameter</span></span>

<span data-ttu-id="d20b3-114">Wenn die Ereignishandlerroutine aufgerufen wird, wird der *Status*-Parameter auf einen der folgenden Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d20b3-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d20b3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d20b3-115">Value</span></span></p></th>
<th><p><span data-ttu-id="d20b3-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d20b3-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d20b3-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="d20b3-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="d20b3-118">Wird den Ereignissen Will und Complete übergeben.</span><span class="sxs-lookup"><span data-stu-id="d20b3-118">Passed to both Will and Complete events.</span></span> <span data-ttu-id="d20b3-119">Dieser Wert bedeutet, dass die Operation, durch die das Ereignis verursacht wurde, erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d20b3-119">This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d20b3-120"><strong>adStatusErrorsOccurred festgelegt</strong></span><span class="sxs-lookup"><span data-stu-id="d20b3-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="d20b3-121">Nur an vollständige Ereignisse übergeben.</span><span class="sxs-lookup"><span data-stu-id="d20b3-121">Passed to Complete events only.</span></span> <span data-ttu-id="d20b3-122">Dieser Wert gibt an, dass der Vorgang, der das Ereignis verursacht hat, fehlgeschlagen ist oder dass der Vorgang durch ein Ereignis abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="d20b3-122">This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation.</span></span> <span data-ttu-id="d20b3-123">Weitere Informationen finden Sie im Parameter <em>Error</em> .</span><span class="sxs-lookup"><span data-stu-id="d20b3-123">Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d20b3-124"><strong>adStatusCantDeny festgelegt</strong></span><span class="sxs-lookup"><span data-stu-id="d20b3-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="d20b3-125">Wird nur Will-Ereignissen übergeben.</span><span class="sxs-lookup"><span data-stu-id="d20b3-125">Passed to Will events only.</span></span> <span data-ttu-id="d20b3-126">Dieser Wert bedeutet, dass die Operation vom Will-Ereignis nicht abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d20b3-126">This value means that the operation cannot be canceled by the Will event.</span></span> <span data-ttu-id="d20b3-127">Sie muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d20b3-127">It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d20b3-128">Wenn Sie in Ihrem Fall Ereignis festlegen, dass der Vorgang fortgesetzt werden soll, lassen Sie den Parameter *Status* unverändert.</span><span class="sxs-lookup"><span data-stu-id="d20b3-128">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged.</span></span> <span data-ttu-id="d20b3-129">Solange der Parameter "eingehender Status" nicht auf **adStatusCantDeny festgelegt**festgelegt ist, können Sie den ausstehenden Vorgang abbrechen, indem Sie *Status* in **adStatusCancel fest**ändern.</span><span class="sxs-lookup"><span data-stu-id="d20b3-129">As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**.</span></span> <span data-ttu-id="d20b3-130">Wenn Sie dies tun, hat das Complete-Ereignis, das dem Vorgang zugeordnet ist, den *Status* -Parameter auf **adStatusErrorsOccurred festgelegt**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d20b3-130">When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**.</span></span> <span data-ttu-id="d20b3-131">Das **Error** -Objekt, das an das Complete-Ereignis übergeben wird, enthält den Wert **adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="d20b3-131">The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="d20b3-p108">Wenn ein Ereignis nicht mehr verarbeitet werden soll, können Sie *Status* auf **adStatusUnwantedEvent** festlegen, und die Anwendung empfängt keine Benachrichtigungen mehr für dieses Ereignis. Manche Ereignisse können jedoch aus mehreren Gründen ausgelöst werden. In diesem Fall müssen Sie **adStatusUnwantedEvent** für jeden möglichen Grund angeben. Zum Beenden des Empfangs von Benachrichtigungen zu ausstehenden **RecordChange**-Ereignissen z. B. müssen Sie den *Status*-Parameter für die auftretenden Ereignisse **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** und **adRsnFirstChange** auf **adStatusUnwantedEvent** festlegen.</span><span class="sxs-lookup"><span data-stu-id="d20b3-p108">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event. Remember, however, that some events can be raised for more than one reason. In that case, you must specify **adStatusUnwantedEvent** for each possible reason. For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d20b3-136">Wert</span><span class="sxs-lookup"><span data-stu-id="d20b3-136">Value</span></span></p></th>
<th><p><span data-ttu-id="d20b3-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d20b3-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d20b3-138"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="d20b3-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="d20b3-139">Es wird angefordert, dass dieser Ereignishandler keine weiteren Benachrichtigungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="d20b3-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d20b3-140"><strong>adStatusCancel fest</strong></span><span class="sxs-lookup"><span data-stu-id="d20b3-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="d20b3-141">Es wird angefordert, dass die Operation, die gerade auftreten soll, abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="d20b3-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="d20b3-142">Error-Parameter</span><span class="sxs-lookup"><span data-stu-id="d20b3-142">Error Parameter</span></span>

<span data-ttu-id="d20b3-143">Der *Error* -Parameter ist ein Verweis auf ein ADO- [Error](error-object-ado.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d20b3-143">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="d20b3-144">Wenn der Parameter *Status* auf **adStatusErrorsOccurred festgelegt**festgelegt ist, enthält das **Error** -Objektdetails dazu, warum der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="d20b3-144">When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed.</span></span> <span data-ttu-id="d20b3-145">Wenn das mit einem Complete-Ereignis verknüpfte will-Ereignis den Vorgang abgebrochen hat, indem Sie den *Status* -Parameter auf **adStatusCancel fest**, wird das Error-Objekt immer auf **adErrOperationCancelled**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d20b3-145">If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="d20b3-146">Object-Parameter</span><span class="sxs-lookup"><span data-stu-id="d20b3-146">Object Parameter</span></span>

<span data-ttu-id="d20b3-p110">Jedes Ereignis empfängt eines oder mehrere Objekte, die die Objekte darstellen, die an der Operation beteiligt sind. Beispielsweise empfängt das **ExecuteComplete**-Ereignis ein **Command**-Objekt, ein **Recordset**-Objekt und ein **Connection**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d20b3-p110">Each event receives one or more objects representing the objects that are involved in the operation. For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="d20b3-149">Reason-Parameter</span><span class="sxs-lookup"><span data-stu-id="d20b3-149">Reason Parameter</span></span>

<span data-ttu-id="d20b3-150">Der *reason* -Parameter \*\*, bereason, enthält zusätzliche Informationen darüber, warum das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d20b3-150">The *Reason* parameter, *adReason*, provides additional information about why the event occurred.</span></span> <span data-ttu-id="d20b3-151">Ereignisse mit einem \*\* Parameter "bereason" können mehrmals aufgerufen werden, selbst für denselben Vorgang, und zwar aus einem anderen Grund.</span><span class="sxs-lookup"><span data-stu-id="d20b3-151">Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason.</span></span> <span data-ttu-id="d20b3-152">Der **WillChangeRecord** -Ereignishandler wird beispielsweise für Vorgänge aufgerufen, die das Einfügen, löschen oder Ändern eines Datensatzes übernehmen oder rückgängig machen.</span><span class="sxs-lookup"><span data-stu-id="d20b3-152">For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record.</span></span> <span data-ttu-id="d20b3-153">Wenn Sie ein Ereignis nur dann verarbeiten möchten, wenn es aus einem bestimmten Grund auftritt, können Sie den \*\* Parameter "bereason" verwenden, um die Vorkommen zu filtern, die Sie nicht interessieren.</span><span class="sxs-lookup"><span data-stu-id="d20b3-153">If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in.</span></span> <span data-ttu-id="d20b3-154">Wenn Sie beispielsweise Daten Satz Änderungsereignisse nur dann verarbeiten möchten, wenn Sie auftreten, weil ein Datensatz hinzugefügt wurde, können Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="d20b3-154">For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

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

<span data-ttu-id="d20b3-p112">In diesem Fall kann die Benachrichtigung potenziell aus jedem der anderen Gründe auftreten. Sie tritt jedoch nur ein Mal für jeden Grund auf. Wenn die Benachrichtigung für jeden Grund ein Mal aufgetreten ist, empfangen Sie nur Benachrichtigungen für die Hinzufügung eines neuen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="d20b3-p112">In this case, notification can potentially occur for each of the other reasons. However, it will occur only once for each reason. After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="d20b3-158">Dagegen müssen Sie *adStatus* nur ein Mal auf **adStatusUnwantedEvent** festlegen, um anzufordern, dass ein Ereignishandler ohne **adReason**-Parameter keine Benachrichtigungen mehr empfängt.</span><span class="sxs-lookup"><span data-stu-id="d20b3-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

